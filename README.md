### Requirements
- Ansible installed (via homebrew)

### To Run

``` bash
$ git clone https://github.com/morochena/mac-dev-setup.git ~/mac-dev-setup
$ cd ~/mac-dev-setup
$ ansible-galaxy install -r requirements.yml
$ ansible-playbook playbook.yml --ask-become-pass

$ source ~/.zshrc
$ sh postinstall.sh 
```

Additional steps:
- set fira code as default iterm2 font
- configure git

- github access
- aws access

- set the following in your .zshrc:
`export NODE_OPTIONS="--max-old-space-size=8000"`

### Run ES, Mongo, Redis
``` bash
$ cd ~/mac-dev-setup/deps-Formability
$ docker-compose up -d
```
