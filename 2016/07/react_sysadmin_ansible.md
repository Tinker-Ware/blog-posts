In this exercise you will learn a bit about Ansible and how to use it
to automate tasks.

You will only need to automate a few of them. Make sure you do it
below the comment line marking what to do there.

<!-- Make sure you're in the correct path. -->

<!-- `cd /opt/tinker/shared_files/tinkerware_react/react-tutorial/` -->

If you think you have a mess in your `deploy-exercise` folder,
delete it, create it again and clone again:

https://github.com/Tinker-Ware/summerschool-infrastructure.git

and run:
```
git checkout automation
```

edit to `provisioning/roles/react_page/tasks/main.yml`

There are a bunch of commented lines explainig what to do below them.

(create user, greate group... )

Now you need to review Ansible documentation for the stuff you want to
automate.

Here's the link on how to create a USER
http://docs.ansible.com/ansible/user_module.html

Basically add line like the following in the correct place.

`- user: name=johnd comment="John Doe" group=admin`

Here are the links of other modules you will need. Check them out.
http://docs.ansible.com/ansible/group_module.html

http://docs.ansible.com/ansible/apt_module.html

http://docs.ansible.com/ansible/git_module.html


Now tell the vagrant machine to apply this role you created to your new node:

edit `provisioning/site.yml` and in the roles part add:
- react

Ready.

Now run
` vagrant up tinkerware.react`

See the magic working automagically.

Inside the vagrant machine, take a look to the log file that will show the status
of the react page.
This can be done with:

```
tail -f /tmp/react.log
```

Once it's finished, visit again 192.168.33.16:3000 and everything should be working fine.

Done.

Easy right?
