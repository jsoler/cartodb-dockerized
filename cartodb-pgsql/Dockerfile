FROM jsoler/cartodb-base:0.1

# dependencias transverles
/*sudo locale-gen en_US.UTF-8
sudo update-locale LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8

sudo apt-get install autoconf binutils-doc bison build-essential flex
sudo apt-get install git
sudo apt-get install python-software-properties*/

# dependencias contenedor de base de datos
sudo add-apt-repository ppa:cartodb/postgresql-9.3 && sudo apt-get update
sudo apt-get install libpq5 \
                     libpq-dev \
                     postgresql-client-9.3 \
                     postgresql-client-common

sudo apt-get install postgresql-9.3 \
                     postgresql-contrib-9.3 \
                     postgresql-server-dev-9.3 \
                     postgresql-plpython-9.3

# configurar acceso a postgresql
# /etc/postgresql/9.3/main/pg_hba.conf

sudo service postgresql restart

sudo createuser publicuser --no-createrole --no-createdb --no-superuser -U postgres
sudo createuser tileuser --no-createrole --no-createdb --no-superuser -U postgres


# instalar extension cartodb
git clone https://github.com/CartoDB/cartodb-postgresql.git
cd cartodb-postgresql
git checkout <LATEST cartodb-postgresql tag>
sudo make all install


#instalar gis
sudo add-apt-repository ppa:cartodb/gis && sudo apt-get update
#Install Proj
sudo apt-get install proj proj-bin proj-data libproj-dev
#Install JSON
sudo apt-get install libjson0 libjson0-dev python-simplejson
#Install GEOS
sudo apt-get install libgeos-c1v5 libgeos-dev
#Install GDAL
sudo apt-get install gdal-bin libgdal1-dev libgdal-dev
sudo apt-get install gdal2.1-static-bin


#instalar postgis
sudo apt-get install libxml2-dev
sudo apt-get install liblwgeom-2.1.8 postgis postgresql-9.3-postgis-2.2 postgresql-9.3-postgis-scripts
