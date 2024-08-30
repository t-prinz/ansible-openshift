# Various playbooks to manage OpenShift

## The playbook to create an OpenShift Project and apply a role for a service account requires the kubernetes python library and can be installed using

    pip install -r requirements.txt

Before running the playbook, make a copy of the example inventory file and update the host and api key.

Run the playbook using

    ansible-playbook -i inventory.yml create-project.yml

## To test passing variables using curl

    curl -s -k --user 'admin:your-password' -H "Content-Type: application/json" -X POST https://aapcont.example.com:8443/api/v2/job_templates/54/launch/ --data '{"extra_vars": {"ocp_clustername": "ocpsandbox", "ocp_baseDomain": "example.com"}}' | jq

## Reference to install OCP on AWS with bare metal nodes

https://www.redhat.com/en/blog/openshift-virtualization-on-amazon-web-services
