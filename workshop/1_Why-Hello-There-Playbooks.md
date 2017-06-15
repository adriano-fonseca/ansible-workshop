## Ok, Ad Hoc might come in handy, but I can't work like that!

#### Say Hello To My Little Friend: "Playbooks"

Playbooks are YAML files that declaratively express tasks to run on a set of hosts

A YAML file allows a simple human readable syntax, is easy to read and write, but it has some [GOTCHAS](http://docs.ansible.com/ansible/YAMLSyntax.html#gotchas) which are worth reading up on.

Here's a small example:

```
---
- name: Initial playbook
  hosts: ansible-workshop
  tasks:
   - ...
```

Let's run a sample playbook we added in the `workshop/examples` folder called `0_initial.yml`:

```
ansible-playbook -i ansible ./workshop/complete_examples/0_initial.yml
```

#### What the, WAT, WHAT IS THAT COW???

Oh that, yes, ahem, that's `cowsay`.

```

ok: [ansible-workshop]
 ___________________
< TASK: Ping server >
 -------------------
        \   ^__^
         \  (oo)\_______
            (__)\       )\/\
                ||----w |
                ||     ||

```

If that's installed (and it should be!), then Ansible uses that for outputting playbook tasks.

If you for some strange reason don't want to bless your eyes with this amazing cow, do the following:

```
export ANSIBLE_NOCOWS=1
```

Let's run that again now

```
ansible-playbook -i ansible ./workshop/complete_examples/0_initial.yml
```

```
TASK: [Ping server] ***********************************************************
ok: [ansible-workshop]
```

Ok, that's a bit slimmer and better.

**NOTE:** That can be disabled permanently in the ansible configuration, see [here](http://docs.ansible.com/intro_configuration.html#nocows) for details. 
Although all the cool kids are using `export ANSIBLE_COW_SELECTION=random`

#### Enough with the Cows, what did we do here exactly?

We ran `ansible-playbook`, with the parameter `-i`, which tells `ansible-playbook` where to find an inventory file/directory.
Then we stated the playbook we want to run.

#### What's an inventory?

An inventory is a configuration file that states the hosts to be used, where you also can state groups of servers, and override parameters for hosts and/or groups.
In our case it's an executable python file that returns the current docker container we are using.

#### Ok, what was that we ran?

Let's have a looksie at the playbook:

```
---
- name: Initial playbook
  hosts: ansible-workshop
  tasks:
    - name: Ping server
      ping:
```

We asked Ansible to run the _ansible-workshop_ host, and ping that server.

**NOTE:** *The Ansible `ping` module doesn't actually run the ping command, just verifies that ansible can connect via ssh/docker to the host.*

**YET ANOTHER NOTE:** *The examples from now on will not explicitly use the `-i ansible` syntax, as we wrote that in the `ansible.cfg` file.*


#### Well that did a can of whoop-nothing!

True dat, let's actually install something, [Nginx](./2_Lets-install-Nginx.md) perhaps?
