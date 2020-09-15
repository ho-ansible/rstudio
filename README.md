# Ansible role: rstudio
RStudio Server web-based IDE for
the R statistical language.

## DEPRECATED
Installation of this app has been moved to kubernetes,
so this ansible role is no longer maintained.

## Requirements
Only tested on Debian buster.

## Role variables
+ `rstudio_ver` (default: auto-updates to latest): which version of 
  RStudio Server to install
+ `rstudio_user` (default: rstudio): unprivileged user to run server
+ `rstudio_passwd` (default: disabled): encrypted password for above user.
  This does not password-protect web access to RStudio.
+ `rstudio_group` (default: rstudio_users): user group for above user
+ `rstudio_host` (default: rstudio): virtual host nginx should listen for
+ `rstudio_localport` (default: 8787): port the RStudio server listens on,
  and where the nginx proxy connects to.  Not public.
+ `rstudio_listen` (default: "localhost:80"): list of nginx 'listen'
  directives; this is the public access.
+ `rstudio_url` (default: rstudio.com repository): where to fetch 
  .deb package from

## Playbooks
+ `main.yml`: apply role

## Dependencies
+ [ho-ansible.nginx](https://github.com/ho-ansible/nginx)
+ [ho-ansible.R](https://github.com/ho-ansible/R)

## License
MIT

## Author Information
Sean Ho, https://github.com/ho-ansible/
