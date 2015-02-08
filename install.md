To run:

1) install boto

    pip install boto

2) in your bash_profile add AWS Keys & source ie.

    export AWS_ACCESS_KEY_ID=''
    export AWS_SECRET_ACCESS_KEY=''

2) run on control system:

    ansible-playbook -i inventory/ec2env site.yml