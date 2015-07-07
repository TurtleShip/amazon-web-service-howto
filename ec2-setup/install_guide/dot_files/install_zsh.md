# Install oh-my-zsh

[Official oh-my-zsh site](http://ohmyz.sh/)

```sh
sudo passwd ec2-user # set password for ec2-user  
sudo yum install zsh # install zsh
curl -L http://install.ohmyz.sh | sh # install oh-my-zsh
chsh -s /bin/zsh # change default login shell
cat /etc/passwd # check that default login shell has changed
exit # logout of ec2 box
ssh -i my-key-pair.pem ec2-user@my-elastic-ip # log back to ec2 box. You should see change in your shell (it should be zsh)
```

Add the below lines to your ```~/.zshrc``` file if you would like.

```sh
ZSH_THEME="muse" # set a muse theme

# Reload zshell
alias reload='source ~/.zshrc'

# openup zshrc
alias vim_zsh='vim ~/.zshrc'
```

Add ```TERM=xterm-color``` to ```~/.zlogin``` if you see **"Terminal is not fully functional"**.
