To run:

1) install boto

    pip install boto

2) in your bash_profile add AWS Keys & source ie.

    export AWS_ACCESS_KEY_ID=''
    export AWS_SECRET_ACCESS_KEY=''

3) run on control system:

    ansible-playbook -i inventory/ec2env site.yml


Note: Make sure inventory is updated with correct appserver(s)


Test out ForwardAgent with git module:

1) Make sure step 2 is setup in above.

2) Make sure to update intventory with correct app server.

3) run on control system:

    ansible-playbook -i inventory/ec2env deploy.yml