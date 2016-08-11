## Ansible IL - Hands on workshop for Beginners

<pre>

 
                ..,:::,,,:::,..                ...,::,,,,::,...
             .,:.             .,,.          ..:.              .:..
         .,,    ,8MMMMMMMMMN,    ,,.     .:.    IMMMMMMMMMMI     :.
        .,,   +MMMMMMMMMMMMMMMMM$   :.. .:    MMMMMMMMMMMMMMMMMM    :.
       .:   IMMMMMMMMMMMMMMMMMMMMM+  .,.,   MMMMMMMMMMMMMMMMMMMMMM   ...
       .,  .MMMMMMMMMMMMMMMMMMMMMMMMM   .  ZMMMMMMMMMMMMMMMMMMMMMMMMM   :.
      .:  DMMMMMMMMMMMMMMMMMMMMMMMMMMM.   NMMMMMMMMMMMMMMMMMMMMMMMMMMM.  ,
     .:  7MMMMMMMMMMMMMMMMMMMMMMMMMMMMM  8MMMMMMMMMMMMMMMMMMMMMMMMMMMMM  .,
     .  =MMMMMMMMMMMMMMMMMMMMMMMMMMMMMMM$MMMMMMMMMMMMMMMMMMMMMMMMMMMMMMM  :.
    .:  MMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMM? ..
    .,  MMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMM  ,
    .. ?MMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMM  :.
    ,. DMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMM  :.
    ,  MMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMM  7MMMMMMMMMMMMMMMMMMMMMMMMMMMMMMM  ,.
    ,  MMMMMMMMMMMMMMMMMMMMMMMMMMMMMMM    MMMMMMMMMMMMMMMMMMMMMMMMMMMMMMM  ,.
    ,. DMMMMMMMMMMMMMMMMMMMMMMMMMMMMMD     MMMMMMMMMMMMMMMMMMMMMMMMMMMMMM  :.
    .. IMMMMMMMMMMMMMMMMMMMMMMMMMMMMM   ?  ZMMMMMMMMMMMMMMMMMMMMMMMMMMMMM  :.
    .,  MMMMMMMMMMMMMMMMMMMMMMMMMMMM   MM   MMMMMMMMMMMMMMMMMMMMMMMMMMMMM  ,
    .:  MMMMMMMMMMMMMMMMMMMMMMMMMMMM  ?MMM   MMMMMMMMMMMMMMMMMMMMMMMMMMM? ..
     .  ~MMMMMMMMMMMMMMMMMMMMMMMMMM   MMMMO  DMMMMMMMMMMMMMMMMMMMMMMMMMM  :.
     .:  8MMMMMMMMMMMMMMMMMMMMMMMM.  ~MMMMM   MMMMMMMMMMMMMMMMMMMMMMMMM  ..
      .,  MMMMMMMMMMMMMMMMMMMMMMMM     7MMMM   MMMMMMMMMMMMMMMMMMMMMMM=  ,
       ..  MMMMMMMMMMMMMMMMMMMMMM   M~   ?MM?  MMMMMMMMMMMMMMMMMMMMMM,  :.
        ,.  MMMMMMMMMMMMMMMMMMMM,  ?MMM    8M   MMMMMMMMMMMMMMMMMMMM~  :.
         ..  IMMMMMMMMMMMMMMMMMM   MMMMMM.   $  .MMMMMMMMMMMMMMMMMM   :.
          .:   MMMMMMMMMMMMMMMM   MMMMMMMMM      MMMMMMMMMMMMMMMM=  .,.
           .:   $MMMMMMMMMMMMM~  .MMMMMMMMMMM     MMMMMMMMMMMMMM   ,.
            ..,   NMMMMMMMMMMM   MMMMMMMMMMMMMM   MMMMMMMMMMMM.  .,.
              ...   MMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMM.  .:.
               .,.   MMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMM~   :.
                 .,.   MMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMM.   :..
                   .,.   NMMMMMMMMMMMMMMMMMMMMMMMMMMM   .:..
                      .:.   MMMMMMMMMMMMMMMMMMMMMMMM   .:.
                        .,.   DMMMMMMMMMMMMMMMMMMM   .:.
                          .,,   8MMMMMMMMMMMMMMM.  .:.
                            .,.   MMMMMMMMMMMM7   :.
                              .,.   MMMMMMMMN   :.
                                .:   ZMMMMM   .,.
                                  .,  ,MM7   :.
                                   .:      :.
                                    .,.  .:.
                                       ..

</pre>

Prerequisites (To be installed on your laptop):

- [Docker](https://docs.docker.com/engine/installation/) 

  ```
  docker pull bigpanda/ubuntu_with_python
  ```

- [Ansible](http://docs.ansible.com/intro_installation.html) 

  ```
  (sudo) pip install 'ansible>=2.1' docker-py
  ```

  *NOTE*: You'll need Ansible version 2.1 and up

- Then:

  ```
  git clone -b noob-workshop-docker https://github.com/bigpandaio/ansible-workshop
  cd ansible-workshop
  ansible-playbook ./bootstrap/setup.yml
  ```

  Then, to check that it works:

  ```
  ansible-playbook ./bootstrap/test.yml
  ```

  If that fails, run

  ```
  ansible-playbook ./bootstrap/fix_apt.yml
  ansible-playbook ./bootstrap/test.yml
  ```
  ```

## Now what?

See the `workshop` directory, you'll find a series of markdown steps that we'll be going through at the workshop, let's start with [step 0](./workshop/0_AdHoc-Commands.md)


*Enjoy!*
