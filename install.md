To run:

1) install boto

    pip install boto

2) in your bash_profile add AWS Keys & source ie.

    export AWS_ACCESS_KEY_ID=''
    export AWS_SECRET_ACCESS_KEY=''

3) run on control system:

    # To create ec2 volumes on existing instance
    ansible-playbook -i inventory/ec2env site.yml

    # To create a new instance called test-staging (name tag)
    ansible-playbook -i inventory/local new_instance.yml --extra-vars "server_name=test-staging"


Note: Make sure inventory is updated with correct appserver(s)


Test out ForwardAgent with git module:

1) Make sure step 2 is setup in above.

2) Make sure to update intventory with correct app server.


3) Make sure ~/.ssh/config contains:

Host *
    ForwardAgent yes


4) run ssh-add on your ssh key that you want to use

5) run on control system:

    ansible-playbook -i inventory/ec2env deploy.yml


References: http://thinkingeek.com/2014/05/10/create-configure-ec2-instances-rails-deployment-ansible/