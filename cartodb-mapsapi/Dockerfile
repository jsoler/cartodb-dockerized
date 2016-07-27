FROM ubuntu:12.04.5
12.04 x64

# dependencias transverles
sudo locale-gen en_US.UTF-8
sudo update-locale LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8

sudo apt-get install autoconf binutils-doc bison build-essential flex
sudo apt-get install git
sudo apt-get install python-software-properties


# dependencias nodejs
sudo add-apt-repository ppa:cartodb/nodejs-010 && sudo apt-get update
sudo apt-get install nodejs

sudo apt-get install libpango1.0-dev

# instalacion maps-API
git clone git://github.com/CartoDB/Windshaft-cartodb.git
cd Windshaft-cartodb
git checkout master

npm install

cp config/environments/development.js.example config/environments/development.js

node app.js development
