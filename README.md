# ansible-ec2
Ansible aws ec2 testing

# install awscli on os x
> $ brew install awscli                                                                                  [±master]
==> Downloading https://homebrew.bintray.com/bottles/awscli-1.9.5.el_capitan.bottle.tar.gz
######################################################################## 100.0%
==> Pouring awscli-1.9.5.el_capitan.bottle.tar.gz
==> Caveats
The "examples" directory has been installed to:
  /usr/local/share/awscli/examples

Add the following to ~/.bashrc to enable bash completion:
  complete -C aws_completer aws

Add the following to ~/.zshrc to enable zsh completion:
  source /usr/local/share/zsh/site-functions/_aws

Before using awscli, you need to tell it about your AWS credentials.
The easiest way to do this is to run:
  aws configure

More information:
  https://docs.aws.amazon.com/cli/latest/userguide/cli-chap-getting-started.html

zsh completion has been installed to:
  /usr/local/share/zsh/site-functions
==> Summary
🍺  /usr/local/Cellar/awscli/1.9.5: 2261 files, 24M

## configure aws cli

mkdir ~/.aws
cd ~/.aws
aws configure

martin@Lius-MacBook-Pro ~/.aws                                                                           [1:26:28]
> $ cat config
[default]
region=ap-southeast-1
output=json

[profile cli-martin]
region=ap-southeast-1
output=text

export AWS_DEFAULT_PROFILE=cli-martin
aws ec2 describe-instances --profile cli-martin
