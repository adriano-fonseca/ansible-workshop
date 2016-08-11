## Where did that value come from?

One of the biggest got'cha with Ansible is when you're using a variable that suddenly has a value you didn't expect.

Although Ansible has a very defined order of variable loading, remembering that order isn't easy.

We'll try it out with a small exercise:

```sh
cp -r ./workshop/complete_examples/step_7/dev/*_vars ./dev/
cp -r ./workshop/complete_examples/step_7/roles/varz ./roles/
cp ./workshop/complete_examples/step_7/varz.yml ./
```

Run this with:

```sh
ansible-playbook ./varz.yml
```

All this role does is to print out the variable `test_var`.

We can also pass that variable as a parameter to the playbook:

```sh
ansible-playbook ./varz.yml -e test_var=ZOMG32
```

### Hmm, where, what, how

We've planted `test_var` definitions ALL OVER THE PLACE.

Each one contains a hint to where the file is.

Comment out the definition of `test_var` according the message you get when running, UNT ZEN: RINSE, REPEAT!!1

![AGAIN, AGAIN](https://github.com/bigpandaio/ansible-workshop/blob/apprentice-workshop-docker/memez/never-ending-facepalm.gif?raw=true)

_THIS WILL TAKE A WHILE!!1_

Then run again with passing a parameter.

### That was intense, need something to relax?

You're absolutely right, [Security Time](./8_hide_all_secrets.md)!
