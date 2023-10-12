# Playbook to create an OpenShift Project and apply a role for a service account

This does require the kubernetes python library and can be installed using

    pip install -r requirements.txt

Before running the playbook, make a copy of the example inventory file and update the host and api key.

Run the playbook using

    ansible-playbook -i inventory.yml create-project.yml
