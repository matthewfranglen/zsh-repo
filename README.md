# ZSH Builder

This will build the latest tag of ZSH to a debian package.

## Installation

Ensure you have a recent version of [Vagrant](https://www.vagrantup.com/downloads.html) and [Ansible](http://docs.ansible.com/intro_installation.html#latest-releases-via-pip) installed. This also requires ZSH, which can be installed using your package manager.

        git clone https://github.com/matthewfranglen/zsh-repo
        vagrant box add ubuntu/precise64 --provider virtualbox
        vagrant box add ubuntu/trusty64 --provider virtualbox

## Execution

        bin/update

OR

        bin/update-repo && bin/build && bin/build-deb

### update-repo

This will clone or update the ZSH repository.

This will exit with failure if there is no new tag available.

### build

This will build ZSH to the target directory.

### build-deb

This will create a .deb file out of the target directory.

This assumes that the src/repo folder has not been altered since ZSH was built, as it gets the version number from there.
