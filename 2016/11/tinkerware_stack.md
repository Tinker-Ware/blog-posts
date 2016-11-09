Tinkerware Technologies Stack
===

Here we describe technologies we've been using and how we use them. Why?
To let people know how we do things.

Basically all of [our open source code](https://github.com/Tinker-Ware) is availabe at GitHub,
and we work to keep everything as open as it gets.

[Here](https://blog.tinkerware.io/tinkerware-tech-principles/) are described more [Tinkerware principles](https://blog.tinkerware.io/tinkerware-tech-principles/) we like to follow such as transparency.

Frontend
---

### React

---

We want to keep things well structured when it comes to Frontend. That way the UX
gets easier to implement and the functionality is easy to grow as well. It's a
very robust Framework if used correctly.

Backend
---

### Elixir

---

Cool, huh? It is. The architectural characterstics that elixir brings to the game
are just what we need to ensure we make things robust and trust worthy thanks to
it's ease of use when programming and it's resilence.


### GoLang

---

Yup. Cool as well. We need concurrence power with the services we provide and
GoLang is the perfect option for this. Also it makes things easier when we need
to make something portable.

Infrastructure
---

We created a Microservices/RPC/Client-server architecture that we use to handle
all the tasks our services does.

### Ansible/Puppet

---

That's how we automate most of the tools we provide to be able to configure
and manage servers at please. You'll be able to find these roles on our
GitHub page. (Link at the beginning of the post)

### Vagrant

---

That's how we are currently virtualizing our Development environment.
To be sure to be working under the same characteristics as our QA/Prod
environments and Integrate changes smoothly.

### Buildbot

---

Our CI/CD robot. We decided to use it because we like to work with Python.
We tried Jenkins before as well and we only use it now for a prototype we
built in the past.

### Server Providers

---

Mostly we use Digital Ocean and AmazonAWS. Why? Depending on the task they are
quite flexible for us, and of course, as any company, we pay attention to the
prices as well.



To be honest, we use our own service! That's how it's supposed to work, isn't it?

And.. we want to keep things as simple as we can...

@aalvz
