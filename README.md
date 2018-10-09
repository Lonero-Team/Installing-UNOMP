# Installing-UNOMP
This is a simple installation guide for people wanting to set up their own UNOMP pools.

First off from their repo -->

```
sudo apt-get install build-essential libssl-dev npm nodejs nodejs-legacy
curl https://raw.githubusercontent.com/creationix/nvm/v0.16.1/install.sh | sh
source ~/.profile
nvm install 0.10.25
nvm use 0.10.25
git clone https://github.com/UNOMP/unified-node-open-mining-portal.git unomp
cd unomp
npm update
```

### Running UNOMP:

Use the `node init.js` command to run

### Tools
Installing Posix: `npm install posix`

Installing bindings: `npm install bindings`

Bignum: `npm install bignum`

### Running Redis: 
https://www.digitalocean.com/community/tutorials/how-to-install-and-use-redis

```
wget http://download.redis.io/releases/redis-stable.tar.gz
tar xzf redis-stable.tar.gz
cd redis-stable
make
sudo make install
cd utils
sudo ./install_server.sh
sudo service redis_6379 start
sudo service redis_6379 stop
```

Accessing the Redis CLI: type `redis-cli`

### Troubleshooting
If you have the "eaccess" or access denied errors try using:
```
sudo npm install enterpackagename
```
```
sudo npm install -g enterpackagename
```
```
sudo npm install -g enterpackagename --allow-root
```

##### Install node-gyp and use `node-gyp rebuild` to rebuild corrupted repos, or run the `npm install` command to reinstall the node modules

##### If you can't do `sudo npm install` or `sudo npm install -g`, try force sudo:
```
sudo npm install -g -unsafe-perm=true --allow-root
```
##### Force installing bindings
```
sudo npm install -g bindings -unsafe-perm=true --allow-root
```
