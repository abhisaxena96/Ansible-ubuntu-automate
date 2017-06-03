````
scp -r .ssh/ root@89.33.6.129:/root/
cd .ssh
rm -rf authorized_keys
cp id_rsa.pub authorized_keys
chmod 600 authorized_keys
port change to 1310
service ssh restart

sudo apt-get install -y vim python-pip figlet sysvbanner  git-core zsh curl git vim-common zip libfontconfig

wget https://github.com/robbyrussell/oh-my-zsh/raw/master/tools/install.sh -O - | zsh
chsh -s `which zsh`

vi .zshrc

ZSH_THEME="steeef"

plugins=(git z zsh-completions osx zsh-autosuggestions  tree cp command-not-found git-extras gnu-utils history terraform pip python ruby screen svn composer aws npm node common-aliases cp copyfile copydir github grunt sudo ubuntu autojump)

reboot


git clone git://github.com/zsh-users/zsh-autosuggestions $ZSH_CUSTOM/plugins/zsh-autosuggestions

git clone https://github.com/zsh-users/zsh-completions ~/.oh-my-zsh/custom/plugins/zsh-completions
vi .zshrc
plugins=(… zsh-completions)
autoload -U compinit && compinit


#configure aws cli
aws configure --profile azz

sudo apt-get install software-properties-common python-software-properties
sudo apt-get install -y language-pack-en-base
sudo LC_ALL=en_US.UTF-8 add-apt-repository ppa:ondrej/php
sudo apt-add-repository ppa:ansible/ansible
sudo apt-get update
sudo apt-get install ansible
sudo apt-get -y --force-yes install php7.0-fpm php7.0 php7.0-common php7.0-cli php7.0-curl php7.0-gd php7.0-gmp php7.0-imap php7.0-intl php7.0-mcrypt php7.0-readline php7.0-xmlrpc php7.0-xsl php7.0-json php7.0-mysql php7.0-opcache php-apcu php-redis php-apcu-bc php-amqp php7.0-bz2 php7.0-bcmath php7.0-mbstring php7.0-soap php7.0-xml php7.0-zip php-pear php-mongodb pkg-config

curl -sS https://getcomposer.org/installer | sudo php -- --install-dir=/usr/local/bin --filename=composer

sudo pip install awscli --ignore-installed six

apt-get install terraform
apt-get install ansible
apt-get install packer
apt-get install docker
apt-get install docker-compose
apt-get install terraforming
apt-get install docker-machine

##NODE
curl -sL https://deb.nodesource.com/setup_7.x | sudo -E bash -
apt-get install nodejs



mkdir workspace
cd workspace && mkdir tajawal 
git clone git@github.com:tajawal/devops.git
git clone git@github.com:tajawal/dev-machine.git
git clone git@github.com:tajawal/cms-site.git
git clone git@github.com:tajawal/ci-api.git
git clone git@github.com:tajawal/qa-web-new.git
git clone git@github.com:tajawal/data.git
git clone git@github.com:tajawal/cli-mongo.git


cd workspace && mkdir herosports
git clone git@github.com:anmolnagpal/HeroSports.git devops



