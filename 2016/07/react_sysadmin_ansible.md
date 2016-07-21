In this exercise you will learn a bit about Ansible and how to use it
to automate tasks.

You will only need to automate a few of them. Make sure you do it
below the comment line marking what to do there.

<!-- Make sure you're in the correct path. -->

<!-- `cd /opt/tinker/shared_files/tinkerware_react/react-tutorial/` -->

Clone the repository for this exercise that contains the ansible code
and more things that are needed for the exercise.

`git clone ;fasdlk;gfj-fl;dskh;`

-- up to here the exercise should be almost done, just with a few empty
blocks to fill with the correct ansible automation --

edit to `provisioning/roles/react_page/tasks/main.yml`

There are a bunch of commented lines explainig what to do below them.

(create user, greate group... )

Now you need to review Ansible documentation for the stuff you want to
automate.

Here's the link on how to create a USER
http://docs.ansible.com/ansible/user_module.html

Basically add line like the following in the correct place.

`- user: name=johnd comment="John Doe" group=admin`

<!-- More missing commands for automate the missing parts -->


At the end you should have a file looking like this:

Ansible file to automate react.

Now tell the vagrant machine to apply this role you created to your new node:

edit `provisioning/tinkerware.yml` and in the roles part add:
- react

Ready.

Now run
` vagrant up tinkerware.react`

See the magic working automagically.

visit again 192.168.33.16:3000 and everything should be working fine.

Done.
