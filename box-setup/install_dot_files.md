# Install oh-my-zsh
```sh
sudo passwd ec2-user # set password for ec2-user  
sudo yum install zsh # install zsh
curl -L http://install.ohmyz.sh | sh # install oh-my-zsh
chsh -s /bin/zsh #Change default login shell
cat /etc/passwd # Check that default login shell has changed
exit # logout of ec2 box
ssh -i my-key-pair.pem ec2-user@my-elastic-ip # log back to ec2 box. You should see change in your shell (it should be zsh)
```
