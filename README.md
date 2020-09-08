# bash-vim-setting



To include this `bash-vim-setting` in a `Dockerfile`, add

```
# My bash and vim setting
RUN apt-get install -y wget unzip && wget https://github.com/dhkangvclab/bash-vim-setting/archive/master.zip && unzip master.zip && cd bash-vim-setting-master && printf "\n# My custom bash profile\nif [ -f ~/.bashrc_my ]; then\n  . ~/.bashrc_my \nfi\n" >> ~/.bashrc && cp -rf .bashrc_my .bashrc_lscolors .vimrc .vim ~/ && cd .. && rm -rf master.zip bash-vim-setting-master
```



To install on a linux environment, run

```
apt-get install -y wget unzip && wget https://github.com/dhkangvclab/bash-vim-setting/archive/master.zip && unzip master.zip && cd bash-vim-setting-master && printf "\n# My custom bash profile\nif [ -f ~/.bashrc_my ]; then\n  . ~/.bashrc_my \nfi\n" >> ~/.bashrc && cp -rf .bashrc_my .bashrc_lscolors .vimrc .vim ~/ && cd .. && rm -rf master.zip bash-vim-setting-master
```
