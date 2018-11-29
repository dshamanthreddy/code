# code1




Poc --steps

Inventory File
mkdir -p ~/Ansible/ansible
touch ~/Ansible/ansible/hosts
touch ~/.ansible.cfg



Open ~/.ansible.cfg file and add the following lines:

[defaults]
inventory = ~/Ansible/ansible/hosts /n
remote_user = root
ask_sudo_pass= true





-------------------------------
roles
|__ defaults

    |__ main.yml - includes information about default variables used by this role

|__ files        - files which need to be deployed to your hosts without any modification.

|__ templates    - using jinja2 templating system, configuration variables can
               be passed to templates and those modified templates will be
               placed on the hosts

|__ tasks        - each play can contain multiple task, and each task can perform multiple actions.
    |__ main.yml

|__ meta         - environment Description, Author, Licensing Attributes etc. are placed.
    |__ main.yml

|__ vars         - variables as username, folder name are stored in vars.
    |__ main.yml

|__ handlers     - tasks which are executed on completion of other tasks.
               think of them as callbacks.
    |__ main.yml
