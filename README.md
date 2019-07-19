# tmux
tmux dotfiles for better portability and mapping

<a href="https://i.imgur.com/zT4Gvv3.png">
  <img src="https://imgur.com/zT4Gvv3l.png" />
</a>

### What is it?
Its a config for the tmux Terminal Multiplexer if your Terminal doesnt support multiple Windows or splits.

### How to install?

Just clone the Repo to your homefolder and move the .tmux folder and the .tmux.config inside to your $HOME folder.

    $ git clone https://github.com/erikschreier/tmux
    $ cd tmux
    $ sudo mv .tmux .tmux.conf ~/
    $ cd .. && rm -rf tmux
    
### On first use:
The config itself is created to use termite with the zsh shell, if you want to use a different setting you have to change some values.

Before you can use the configs you have to make sure your $TERM value is the same as in ~/.tmux/.tmux.conf.options:

    $  echo $TERM
    >> xterm-256color # depending on your terminal
    
    $ vim ~/.tmux/.tmux.conf.options
    
    13 ..
    14 set -g default-terminal "xterm-256color"  <-- here goes your $TERM value
    15 ..
    
The last Step is to set your default Shell, if you want to use something other than zsh you have to modify line 10 in the same file.

     9 ..
    10 set-option -g default-shell /usr/bin/fish
    11 ..

If you want to use bash instead you just can comment out the line.

### WARNING: New Mapping
In general there are only a few aditions of keys (see ~/.tmux/.tmux.conf.keymaps) but there two changes where experienced users could struggle, see line 12 to 17 and 19 to 27.
