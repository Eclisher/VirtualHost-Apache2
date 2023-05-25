# VirtualHost-Apache2

#### Ansible Apache2 Folder Creation Project
This project aims to automate the creation of folders on Apache2 web server using Ansible. The objective is to simplify the process of setting up new directories on the server, ensuring consistent and efficient folder management.


#### Ansible Apache2 Folder Creation Project

This project aims to automate the creation of folders on Apache2 web server using Ansible. The objective is to simplify the process of setting up new directories on the server, ensuring consistent and efficient folder management.
Prerequisites

#### To run this Ansible playbook, ensure that you have the following prerequisites installed:

- Ansible: Version 2.10 or later.
- Apache2: Installed and properly configured on the target server.
- SSH access: Ensure that you have SSH access to the target server with appropriate credentials.

#### Conclusion

This project provides a convenient way to automate the creation of folders on an Apache2 web server using Ansible. By utilizing this playbook, you can streamline the process of setting up new directories, ensuring consistency and reducing manual effort. Feel free to customize the playbook to fit your specific needs and extend its functionality as required.
## Installing Ansible

1. Ubuntu / Debian :
    ```sh
    sudo apt update
    ```
    ```sh
    sudo apt install ansible

2. CentOS / RHEL :
    ````sh
    sudo yum install epel-release
    ````
    ````sh
    sudo yum install ansible
    `````
3. Fedora :

    ````sh
    sudo dnf install ansible
    ````
4. MacOS (via Homebrew) :

    `````sh
    brew install ansible

5. Windows (via le sous-système Windows pour Linux - WSL) :
-  #### Make sure you have WSL installed and configured on your system.
 - ####   Open a WSL distribution (e.g. Ubuntu) and follow the Ubuntu-specific installation steps mentioned above.    

# Here is the apache configuration if we want to start  the `api.hei.com` ,  `front.hei.com` , `back.hei.com`
<VirtualHost *:80>
    ServerName api.school.com
    DocumentRoot /var/www/api.school.com

    ErrorLog ${APACHE_LOG_DIR}/api_error.log
    CustomLog ${APACHE_LOG_DIR}/api_access.log combined
</VirtualHost>

<VirtualHost *:80>
    ServerName front.hei.school
    DocumentRoot /var/www/front.hei.school

    ErrorLog ${APACHE_LOG_DIR}/front_error.log
    CustomLog ${APACHE_LOG_DIR}/front_access.log combined
</VirtualHost>

<VirtualHost *:80>
    ServerName back.hei.school
    DocumentRoot /var/www/back.hei.school

    ErrorLog ${APACHE_LOG_DIR}/back_error.log
    CustomLog ${APACHE_LOG_DIR}/back_access.log combined
</VirtualHost>
