FROM ubuntu:12.04.5
12.04 x64

# dependencias transverles
sudo locale-gen en_US.UTF-8
sudo update-locale LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8

sudo apt-get install autoconf binutils-doc bison build-essential flex
sudo apt-get install git
sudo apt-get install python-software-properties


#ruby
wget -O ruby-install-0.5.0.tar.gz https://github.com/postmodern/ruby-install/archive/v0.5.0.tar.gz
tar -xzvf ruby-install-0.5.0.tar.gz
cd ruby-install-0.5.0/
sudo make install

sudo apt-get install libreadline6-dev openssl

sudo ruby-install ruby 2.2.3

export PATH=$PATH:/opt/rubies/ruby-2.2.3/bin

sudo gem install bundler

sudo gem install compass

# editor
git clone --recursive https://github.com/CartoDB/cartodb.git
cd cartodb

sudo wget  -O /tmp/get-pip.py https://bootstrap.pypa.io/get-pip.py
sudo python /tmp/get-pip.py

sudo apt-get install python-all-dev
