# Juju Cheatsheet

Sometimes you don't have all day to figure stuff out, here's a TLDR of how to use Juju:

## Installing the PPA and all the goodies:

- `sudo add-apt-repository ppa:juju-stable && sudo apt-get update && sudo apt-get install juju juju-local juju-quickstart charm-tools`
- `juju quickstart -i` - prompts you for all your cloud credentials. 
- `juju bootstrap -v` - bootstrap a node (always -v so you can see what's going on, drop the -v when you get comfortable with juju, but juju bootstrap since 1.17.0 shows what's going on -v is really verbose at this point)
- `juju debug-log` - open this in another terminal or tab, so you can see what juju is doing while you type other commands)

## Using Juju

- `juju deploy $servicename $alias`- deploy a service, alias is optional if you want to name it something. If you use aliases you need to refer to the service via the alias from then on:

                juju deploy mediawiki myawesomewiki

- `juju add-unit $servicename` - add a unit
- `juju add-unit -n 10 $servicename` - add 10 units.
- `juju deploy $servicename --to #` - deploy servicename to a specific machine #. Use 0 to deploy to the bootstrap node.
- `juju status` - shows what's going on
- `juju status servicename` - shows you what's going for a particular server
- `juju ssh servicename/machine#` - ssh to a unit, get the # from juju status
- `juju ssh machine#` - ssh to a machine number
- `juju run "uname -a" --all` - Run a command (uname) on every instance. (1.17.2 and newer)

## bundles

- `juju quickstart bundle:~abentley/wiki-bundle/1/wiki` - Get the bundle address from jujucharms.com

## Relations

- `juju add-relation $service1 $service2` - relate two services
- `juju destroy-relation $service1 $service2` - unrelate 2 services

## Deploying to Containers, VMs, and metal

- `juju deploy servicename --to lxc:10` - Deploy service to a container on machine #10
- `juju deploy servicename --to kvm:10` - Deploy service to a KVM on machine #10
- `juju deploy servicename --to 10` - Deploy service to the raw bare metal on machine #10


## Destroying Stuff

- `juju destroy-environment $environment-name` - destroy an environment
- `juju destroy-service $servicename` - destroy a service, DOES NOT REMOVE THE MACHINE, you need to follow up:
- `juju destroy-machine` # - destroy machine # 

## Writing Charms/Bundles

- `charm create foo` - create a blank charm template
- `charm add tests` - add tests to an existing charm
- `charm add readme` - add a readme template to an existing charm
- `charm proof` - lint for charms
- `bundle proof` - lint for bundles
- `juju debug-hooks` - debug mode for charm writing, this will ssh you into the units and fire off a tmux session to debug (totally awesome, use this). 

## Clean up

- "I broke the local provider and need to start over" - http://askubuntu.com/questions/403618/how-do-i-clean-up-a-machine-after-using-the-local-provider
- "There's a race somewhere and sometimes the unit doesn't come up" - `juju resolved $servicename --retry` 

## Other

- Listing of all the charms: https://jujucharms.com/fullscreen/search/?text=
- `juju status -e $environmentname` - show me the status of another environment
- `juju switch $environmentname` - switch to a different environment
- `juju add-machine` - add a blank machine that you can mess with

## Useful LXC commands

`sudo lxc-ls --fancy` - show all the containers on your machine

# Odd plugins that exist and aren't really documented or packaged anywhere



