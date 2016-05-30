# Vagrantfiles

Multiple Virtual Machine configured for specific languages.

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

| Name   | IP Address   | Content                             |
|--------|--------------|-------------------------------------|
| gui    | 192.168.56.2 | MATE Desktop + Google Chrome + Atom |
| nodejs | 192.168.56.3 | NodeJS + NPM + MongoDB              |
| python | 192.168.56.4 | Python 2.7 + Python 3.4 + Pip       |
