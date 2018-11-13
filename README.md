# Ansible role: rstudio
Web-based remote IDE for R statistical software

## Requirements
Only tested on Debian stable, for now.

## Role Variables
+ `rstudio_ver`: version string as in official download URL. Default is to check for the latest version.
+ `rstudio_user` (default: rstudio): unprivileged user to run server as
+ `rstudio_passwd` (default: no password): password for above user. You should change this! 
+ `rstudio_group` (default: rstudio_users): user group for above user
+ `rstudio_host` (default: rstudio): hostname (virtual host) that nginx listens for
+ `rstudio_localport` (default: 8787): localhost port that the server listens on. Nginx will proxy to this port
+ `rstudio_listen` (default: "localhost:80"): list of lines for nginx "listen" config

## Dependencies
None.

## Example Playbook

```
- hosts: rstudio
  roles:
    - { role: ho-ansible.rstudio }
```

## License
MIT

## Author Information
Sean Ho, https://github.com/ho-ansible/
