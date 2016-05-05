# charm-tools 2.x

This is a summary of the 2.x charm-tools subcommands. For more detailed
information refer to the [charm-tools documentation](https://jujucharms.com/docs/devel/tools-charm-tools).

## Install charm-tools

```sh
sudo add-apt-repository -y ppa:juju/devel
sudo add-apt-repository -y ppa:juju/stable
sudo apt update -qq
sudo apt install -y charm-tools
```

## charm-tools 2.x subcommands
```
add            - add icon, readme, or tests to a charm
attach         - upload a file as a resource for a charm
build          - build a charm from layers and interfaces
create         - create a new charm
grant          - grant charm or bundle permissions
help           - show help on a command or other topic
layers         - inspect the layers of a built charm
list           - list charms for a given user name
list-resources - display the resources for a charm in the charm store
login          - login to the charm store
logout         - logout from the charm store
proof          - perform static analysis on a charm or bundle
publish        - publish a charm or bundle
pull           - download a charm or bundle from the charm store
pull-source    - download the source code for a charm, layer, or interface
push           - push a charm or bundle into the charm store
revoke         - revoke charm or bundle permissions
set            - set charm or bundle extra-info, home page or bugs URL
show           - print information on a charm or bundle
terms          - lists terms owned by the user
test           - execute charm functional tests
version        - display tooling version information
whoami         - display jaas user id and group membership
```

## Using charm-tools

##### `charm add`
- `charm add tests` - Add things to an existing charm, such as icon, tests,
readme (template).

##### `charm attach`
- `charm attach ~user/trusty/wordpress website-data ./foo.zip` - Upload a file
as a resource for a charm.

##### `charm build`
- `charm build` - Build the layers and interfaces into a charm.
