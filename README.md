## Prerequisites

- Docker must be installed on the host system.
- Ansible must be installed on the host system.

## Setup

1. Copy the example variables file and edit it to provide your configuration.

   Copy `.vars.yaml.example` to `.vars.yaml` and fill in the required values, especially `domain_name` and `tls_owner_mail`.

2. Run the playbook to deploy the environment:

   ansible-playbook -i inventory.ini playbook.yml

3. Once the playbook finishes, open your browser and navigate to the domain specified in `domain_name` from `.vars.yaml`.

   For example: https://dc-hm1.eduardmenshikh.ru

4. You should see the WordPress setup page ready to configure your site.

## Cleanup

To delete all Docker containers, networks, and images related to this deployment, run the cleanup playbook:

ansible-playbook -i inventory.ini cleanup.yaml
# distributedComputing_task1
