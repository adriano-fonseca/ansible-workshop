## Bag'Em and Tag'Em

```sh
cp ./workshop/complete_examples/step_6/deploy.yml ./
cp ./workshop/complete_examples/step_6/roles/nginx/tasks/main.yml ./roles/nginx/tasks/
cp ./workshop/complete_examples/step_6/roles/app/tasks/main.yml ./roles/app/tasks/
```

The playbook simply includes all the other playbooks we wrote, but with a twist, it adds tags to the include.

```yaml
---
- include: hosts.yml tags=infra
- include: app.yml tags=app
- include: web.yml tags=web
```

And the other tasks were updated with tags accordingly.

This allows us to run this playbook and specify which tag we want to deploy:

```sh
ansible-playbook deploy.yml --skip-tags infra --tags app
```

### SO MUCH SPEED SO MUCH DOGE

![NOTHING CAN STOP ME!](https://github.com/bigpandaio/ansible-workshop/blob/apprentice-workshop-docker/memez/juggernaut.gif?raw=true)

So now we have a single point for our deployments. We can now use this script via ChatOps or whatever the cool kids are doing.

### Tis' cool. Where's the trap?

The one pitfall you must prepare yourselves for is:

**WHICH VARIABLE OVERRIDES WHICH!?!?**

![WHICH VARIABLE OVERRIDES WHICH!](https://github.com/bigpandaio/ansible-workshop/blob/apprentice-workshop-docker/memez/what-where.jpg?raw=true)

We'll tackle that in [variables everywhere](./7_variables_everywhere.md).
