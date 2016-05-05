# Juju 2.x Cheatsheet

This is a summary of the Juju 2.x subcommands. For more detailed information
refer to the official [Juju documentation](https://jujucharms.com/docs/devel/)

All the juju subcommands have descriptive help, use `juju help $SUBCOMMAND` for
more information about each subcommand.

## Install Juju and charm-tools:

Install the juju package and charm-tools:
```sh
sudo add-apt-repository -y ppa:juju/devel
sudo add-apt-repository -y ppa:juju/stable
sudo apt update -qq
sudo apt install -y juju-2.0
```

## Juju 2.x subcommands:

```
actions                 alias for 'list-actions'
add-cloud               Adds a user-defined cloud to Juju from among known cloud types.
add-credential          Adds or replaces credentials for a cloud.
add-machine             start a new, empty machine and optionally a container, or add a container to a machine
add-machines            alias for 'add-machine'
add-relation            add a relation between two services
add-space               Add a new network space
add-ssh-key             Adds a public SSH key to a model.
add-ssh-keys            alias for 'add-ssh-key'
add-storage             adds unit storage dynamically
add-subnet              add an existing subnet to Juju
add-unit                Adds one or more units to a deployed service.
add-units               alias for 'add-unit'
add-user                Adds a Juju user to a controller.
agree                   agree to terms
allocate                allocate budget to services
attach                  upload a file as a resource for a service
autoload-credentials    looks for cloud credentials and caches those for use by Juju when bootstrapping
backups                 alias for 'list-backups'
block                   list and enable model blocks
bootstrap               Initializes a cloud environment.
cached-images           alias for 'list-cached-images'
change-user-password    changes the password for a user
charm                   interact with charms
collect-metrics         collect metrics on the given unit/service
create-backup           create a backup
create-budget           create a new budget
create-model            create an model within the Juju Model Server
create-storage-pool     create storage pool
debug-hooks             launch a tmux session to debug a hook
debug-log               Displays log messages for a model.
debug-metrics           retrieve metrics collected by the given unit/service
deploy                  deploy a new service or bundle
destroy-controller      Destroys a controller.
destroy-model           Terminate all machines and resources for a non-controller model.
destroy-relation        alias for 'remove-relation'
destroy-service         alias for 'remove-service'
destroy-unit            alias for 'remove-unit'
disable-user            Disables a Juju user.
download-backup         get an archive file
enable-ha               ensure that sufficient controllers exist to provide redundancy
enable-user             Re-enables a previously disabled Juju user.
expose                  Makes a service publicly available over the network.
get-config              Displays configuration settings for a deployed service.
get-configs             alias for 'get-config'
get-constraints         Displays machine constraints for a service.
get-model-config        Displays configuration settings for a model.
get-model-constraints   Displays machine constraints for a model.
grant                   Grants access to a Juju user for a model.
gui                     open the Juju GUI in the default browser
help                    show help on a command or other topic
help-tool               show help on a juju charm tool
import-ssh-key          Adds a public SSH key from a trusted identity source to a model.
import-ssh-keys         alias for 'import-ssh-key'
kill-controller         forcibly terminate all machines and other associated resources for a juju controller
list-actions            list actions defined for a service
list-agreements         list user's agreements
list-all-blocks         list all blocks within the controller
list-backups            get all metadata
list-budgets            list budgets
list-cached-images      shows cached os images
list-clouds             Lists all clouds available to Juju.
list-controllers        Lists all controllers.
list-credentials        Lists credentials for a cloud.
list-machine            alias for 'list-machines'
list-machines           Lists machines in a model.
list-models             Lists models a user can access on a controller.
list-payloads           display status information about known payloads
list-plans              list plans
list-resources          show the resources for a service or unit
list-shares             Shows all users with access to a model for the current controller.
list-spaces             List known spaces, including associated subnets
list-ssh-key            alias for 'list-ssh-keys'
list-ssh-keys           Lists the currently known SSH keys for the current (or specified) model.
list-storage            lists storage details
list-storage-pools      list storage pools
list-subnets            list subnets known to Juju
list-users              Lists Juju users allowed to connect to a controller.
login                   logs in to the controller
logout                  logs out of the controller
machine                 alias for 'list-machines'
machines                alias for 'list-machines'
publish                 publish charm to the store
register                Registers a Juju user to a controller.
remove-all-blocks       remove all blocks in the Juju controller
remove-backup           delete a backup
remove-cached-images    remove cached os images
remove-credential       Removes credentials for a cloud.
remove-machine          remove machines from the model
remove-machines         alias for 'remove-machine'
remove-relation         Removes an existing relation between two services.
remove-service          Remove a service from the model.
remove-ssh-key          Removes a public SSH key (or keys) from a model.
remove-ssh-keys         alias for 'remove-ssh-key'
remove-unit             remove service units from the model
resolved                marks unit errors resolved
resources               alias for 'list-resources'
restore-backup          restore from a backup archive to a new controller
retry-provisioning      retries provisioning for failed machines
revoke                  Revokes access from a Juju user for a model.
run                     run the commands on the remote targets specified
run-action              queue an action for execution
scp                     Transfers files to/from a Juju machine.
set-budget              set the budget limit
set-config              Sets configuration options for a service.
set-configs             alias for 'set-config'
set-constraints         Sets machine constraints for a service.
set-default-credential  Sets the default credentials for a cloud.
set-default-region      Sets the default region for a cloud.
set-meter-status        sets the meter status on a service or unit
set-model-config        Sets configuration keys on a model.
set-model-constraints   Sets machine constraints on a model.
set-plan                set the plan for a service
show-action-output      show results of an action by ID
show-action-status      show results of all actions filtered by optional ID prefix
show-backup             get metadata
show-budget             show budget usage
show-cloud              Shows detailed information on a cloud.
show-controller         Shows detailed information of a controller.
show-controllers        alias for 'show-controller'
show-machine            show a machines status
show-machines           alias for 'show-machine'
show-model              shows information about the current or specified model
show-status             alias for 'status'
show-storage            shows storage instance
show-user               Show information about a user.
spaces                  alias for 'list-spaces'
ssh                     Initiates an SSH session or executes a command on a Juju machine.
ssh-key                 alias for 'list-ssh-keys'
ssh-keys                alias for 'list-ssh-keys'
status                  Displays the current status of Juju, services, and units.
status-history          output past statuses for the passed entity
storage                 alias for 'list-storage'
subnets                 alias for 'list-subnets'
switch                  Selects or identifies the current controller and model.
sync-tools              copy tools from the official tool store into a local model
unblock                 unblock an operation that would alter a running model
unexpose                Removes public availability over the network for a service.
unset-model-config      Unsets model configuration.
update-allocation       update an allocation
update-clouds           Updates public cloud information available to Juju.
upgrade-charm           upgrade a service's charm
upgrade-gui             upgrade to a new Juju GUI version
upgrade-juju            Upgrades Juju on all machines in a model.
upload-backup           store a backup archive file remotely in juju
version                 print the current version
```

## Using juju

##### `juju add-cloud`
- `juju add-cloud mycloud ~/mycloud.yaml` - Add a user defined cloud to Juju.

##### `juju add-credential`

##### `juju add-machine`

##### `juju add-relation`

##### `juju add-space`

##### `juju add-unit`
- `juju add-unit servicename` - add a unit
- `juju add-unit -n 10 servicename` - add 10 units.

##### `juju deploy`
Juju version 2.x has the ability to deploy both charms and bundles.

- `juju deploy servicename alias`- deploy a service, alias is optional if you
 want to name it something. If you use aliases you need to refer to the service
via the alias from then on:  
```sh
juju deploy mediawiki myawesomewiki
```
- `juju deploy path/to/charm --series trusty` - deploy a charm on your **local
filesystem** you must also specify the series.
- `juju deploy path/to/bundle.yaml` - deploy a bundle on your **local
filesystem**.
- `juju deploy servicename --to #` - deploy servicename to a specific machine #. Use 0 to deploy to the bootstrap node.
