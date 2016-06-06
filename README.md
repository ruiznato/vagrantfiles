# Vagrantfiles

[![Build Status](https://travis-ci.org/ruiznato/vagrantfiles.svg?branch=master)](https://travis-ci.org/ruiznato/vagrantfiles)

Multiple Virtual Machine configured for specific languages.
## Requirements
This VMs utilize Vagrant plugin [Host Manager](https://github.com/devopsgroup-io/vagrant-hostmanager). Install it with the following command:
```
vagrant plugin install vagrant-hostmanager
```
In Windows, in order to utilize "rsync" for the sharing folders is recommended to install **Cygwin** or **Baboon**.
## Usage
To start all VMs just clone the repo and execute `vagrant up`.

To start/manage only an specific VM (check the list below):
```
vagrant up gui
vagrant provision nodejs
vagrant halt python
```
Alternatively you can go inside each language directory and start only that VM:
```
cd python
vagrant up
```
You can enable/disable each VM in the main `Vagrantfile`. In the following example the Python VM is disabled:
```
...
begin
  load 'gui/Vagrantfile'
  # load 'python/Vagrantfile'
  load 'nodejs/Vagrantfile'
...
```

## Available languages
All VMs are based on CentOS 7 Minimal

| Name   | IP Address   | Hostname   | Content                             |
|--------|--------------|------------|-------------------------------------|
| gui    | 192.168.56.2 | gui.dev    | MATE Desktop + Google Chrome + Atom |
| nodejs | 192.168.56.3 | nodejs.dev | NodeJS + NPM + MongoDB              |
| python | 192.168.56.4 | python.dev | Python 2.7 + Python 3.4 + Pip       |
| php    | 192.168.56.5 | php.dev    | PHP + MariaDB                       |
