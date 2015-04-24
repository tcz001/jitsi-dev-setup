#jitsi-dev-setup

jitsi-dev-setup is a suitcase for jitsi dev environment provision.

It's using vagrant and ansible to setup following envs

- Ubuntu
- git
- oracle-jdk7
- ant
- apt: name=x11-common state=present
- apt: name=libxi6 state=present
- apt: name=libgconf-2-4 state=present

Make sure you already get vagrant and ansible ready on your machine

```
ansible-galaxy install -r requirements.txt
```

run vagrant up to start your box

```
vagrant up
```

or if you want to use your own box, just copy the playbook.yml to your path and run

```
vagrant provision
```

when finished you can just `vagrant ssh` and clone the repo at `git@github.com:jitsi/jitsi.git`

run ant to build and run

```
ant rebuild run
```
