# role-tomcat

Ansible role for Tomcat 8.5 with optional local web frontend of either Apache or Nginx.

In order to use this role, some of the variables are required to be specified or defined, such as **web_frontend** and **tomcat_bind_ip**. For other variables, please overwrite them as your needs.

| Name                         | Value                | Description                    | File              |
| ---                          | ---                  | ---                            | ---               |
| web_frontend                 | undefined            | apache/nginx or no local web   |                   |
| tomcat_user                  | tomcat               | username of the installation   | defaults/main.yml |
| tomcat_group                 | tomcat               | group name of the installation | defaults/main.yml |
| tomcat_dir                   | /opt/tomcat          | directory of the installation  | defaults/main.yml |
| tomcat_bind_ip               | 127.0.0.1            | binding IP address             | defaults/main.yml |
| tomcat_port                  | 8080                 | port for HTTP                  | defaults/main.yml |
| tomcat_ajp_port              | 8009                 | port for AJP/1.3               | defaults/main.yml |
| tomcat_redirect_port         | 8443                 | port for HTTPS                 | defaults/main.yml |
| tomcat_shutdown_port         | 8005                 | port for shutdown operations   | defaults/main.yml |
| tomcat_java_opts             | ...                  | java opts for tomcat runtime   | defaults/main.yml |
| tomcat_is_readonly           | 'true'               | readonly option                | defaults/main.yml |
| tomcat_auth_enabled          | 'true'               | auth option on AJP connector   | defaults/main.yml |
| tomcat_pkg_name              | apache-tomcat        | name of tomcat package         | defaults/main.yml |
| tomcat_version               | 8.5.43               | version of tomcat package      | defaults/main.yml |
| tomcat_repo_url              | ...                  | url of repo for tomcat package | defaults/main.yml |

By default, **web_frontend** is not defined. In this case, the role assumes the web frontend is on a remote box. If you want to have a local web server installed and configured, set **web_frontend** to either Apache or Nginx. 

## Status

Tested on images of RHEL 7.3 with either Ansible Core 2.6.

## See Also
* [Ansible Docs] (http://docs.ansible.com)
* [role-apache] (https://github.com/yannanlu/role-apache)
* [role-nginx] (https://github.com/yannanlu/role-nginx)
