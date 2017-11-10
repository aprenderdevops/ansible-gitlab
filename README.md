# ansible-gitlab
Instalación de [GitLab](https://about.gitlab.com/) en [CentOS 7 x86_64](https://www.centos.org/) con [Ansible](https://www.ansible.com/).

La instalación se realiza en una máquina virtual [VirtualBox](https://www.virtualbox.org/) utilizando [Vagrant](https://www.vagrantup.com/). Para crear la máquina virtual y lanzar la instalación de GitLab, ejecutar el siguiente comando:
```
$ vagrant up
```

Acceder a GitLab con un navegador a http://localhost:8080

La edición de GitLab a instalar se configura en la variable `gitlab_edition` del fichero `provision/roles/gitlab/defaults/main.yml` y puede tener los siguientes valores:
* `gitlab-ce` para Community Edition (CE)
* `gitlab-ee` para Enterprise Edition (EE)

Funciona tanto con distribuciones Linux basadas en RedHat como en Debian.

---

Tags: ansible, centos, configuration management, devops, gitlab, vagrant, virtualbox