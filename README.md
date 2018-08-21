# Ansible role: rstudio
Installs the RStudio Server web-based IDE for
the R statistical language.

```
rstudio_ver: "{{ lookup('url', rstudio_current) }}"
rstudio_user: rstudio
rstudio_passwd: ''
rstudio_group: rstudio_users
rstudio_host: rstudio
rstudio_localport: 8787
rstudio_listen:
  - "localhost:80"

rstudio_url: "https://download2.rstudio.org/rstudio-server-{{ ansible_distribution_release }}-{{ rstudio_ver }}-amd64.deb"
```
