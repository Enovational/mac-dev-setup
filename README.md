### Requirements

None, if you manually installed apps (eg. Chrome) before running these script you may run into an error. You should manually remove those apps from `config.yml` and try running the commands again as it will cause the rest of the installation to fail. 

These instructions and scripts attempt to be idempotent, so there shouldn't be any issues running them multiple times. 

### To Run

``` bash
$ git clone https://github.com/morochena/mac-dev-setup.git ~/mac-dev-setup
$ cd ~/mac-dev-setup

$ sh preinstall.sh

$ ansible-galaxy install -r requirements.yml
$ ansible-playbook playbook.yml --ask-become-pass

$ source ~/.zshrc
$ sh postinstall.sh 
```

Manual steps after running:
- Set Fira Code as default iTerm2 font
- Configure git name/email 
- set the following in your .zshrc:

``` bash
export NODE_OPTIONS="--max-old-space-size=8000"
eval $(starship init zsh)
```

### Run ElasticSearch, Mongo, Redis
``` bash
$ cd ~/mac-dev-setup/deps-Formability
$ docker-compose up -d
```
