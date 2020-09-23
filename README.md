# Notez

## Chapter 05

### V section 04

chapter 05  
section 04  
**_`models views routes & partials`_**

```bash Ch-05 section 4

# curl -sL https://deb.nodesource.com/setup_14.x | sudo -E bash -
# curl -sL https://deb.nodesource.com/setup_12.x | sudo -E bash -
# curl -sL https://deb.nodesource.com/setup_10.x | sudo -E bash -
# sudo apt purge nodejs
# sudo apt remove nodejs
# sudo apt-get install -y nodejs
npx express-generator --view=hbs --git notez
# npx express-generator@4.x --view=hbs --git notez
cd notez && npm install
npm audit fix
git init
git add .
# npm i hbs@4.1.1
mkdir models
mkdir partials
touch models/Note.js
touch models/notes-memory.js
touch partials/header.hbs
touch routes/notes.js
touch views/noteedit.hbs
touch views/noteview.hbs
touch views/notedestroy.hbs
# DEBUG=notez:* npm start
git remote add origin https://github.com/TurtleWolf/Notez.git
git push -u origin master
git status

```

```bash Ch-05 section 4
 2001  mkdir notez
 2002  cd notez
 2003  npx express-generator@4.x --view=hbs --git .
 2004  npm install
 2005  npm audit
 2007  npm audit fix
 2008  npm audit
 2009  DEBUG=notes:* npm start
 2010  DEBUG=notez:* npm start
 2020  cd ..
 2021  git init
 2022  git status
 2023  git add .
 2024  git status
 2026  code .

 1966  cd notez
 1967  npm i cross-env
 1968  npm start
 1969  mv routes/index.js routes/index.mjs
 1971  mv app.js app.mjs
 1973  touch approotdir.mjs
 1974  touch appsupport.mjs
 1977  mkdir models
 1978  touch models/Notes.mjs
 1979  touch models/notes-memory.mjs
 1981  mkdir partials
 1983  touch partials/header.hbs
 1984  DEBUG=notez:* npm start
 1986  DEBUG=notez:* npm start
 1987  cd notez
 1988  DEBUG=notez:* npm start
 1989  touch routes/notes.mjs
 1990  touch views/noteedit.hbs
 1991  touch views/noteview.hbs
 1992  touch views/notedestroy.hbs
 1993  DEBUG=notez:* npm start
 1994  npm start
 1995  npm run server2
```

---

### V section 05

chapter 05  
section 05  
**_`styles.css`_**

---

### V section 06

chapter 05  
section 06
**_`package.json`_**

---

## Chapter 06

---

### VI section 04

chapter 06  
section 04  
**_`jQuery Poppers BootStrap & assets`_**

```bash Ch-06 section 4

npm i bootstrap jquery popper.js@1.16.x
mkdir public/assets
mv public/images/ public/javascripts/ public/stylesheets/ public/assets/
npm start
npm run server1
npm run server2
```

---

### VI section 06

chapter 06  
section 06  
**_`Mobile-first with feather-icons`_**

```bash Ch-06 section 6

npm i feather-icons
npm start

```

---

### VI section 07

chapter 06  
section 07  
**_`slate theme`_**

<!--
```bash Ch-06 section 7
mkdir theme
touch theme/package.json
touch theme/_custom.scss
cd theme
npm init -y
``` -->

```bash Ch-06 section 7

npm run dl-slate
```

---

## Chapter 07

---

### VII section 03

chapter 07  
section 03  
**_`debug logging`_**

```bash section 3

REQUEST_LOG_FORMAT=common npm start
npm i rotating-file-stream
npm i fs-extra
# npm i util
DEBUG=express:* npm start

```

---

### VII section 04

chapter 07  
section 04  
**_`mjs modules`_**

```bash section 4

mv app.js app.mjs
mv bin/www bin/www.mjs
# cd models
mv models/Note.js models/Note.mjs
mv models/notes-memory.js models/notes-memory.mjs
# cd routes
mv routes/index.js routes/index.mjs
mv routes/notes.js routes/notes.mjs
# npm i esm
# npm -r esm start
# npm uninstall esm

```

<!-- # MAY NOT NEED..
mv app.mjs app.js
mv bin/www bin/www.js
# cd models
mv models/Note.mjs models/Note.js
mv models/notes-memory.mjs models/notes-memory.js
# cd routes
mv routes/index.mjs routes/index.js
mv routes/notes.mjs routes/notes.js -->

---

### VII section 05

chapter 07  
section 05  
**_`storage file_system`_**

```javascript
import * as notes from '../models/notes-memory.mjs';
import * as notes from '../models/notes.mjs';
```

```bash section 5
npm run start-fs
npm run server1
npm run server2
```

---

### VII section 06

chapter 07  
section 06  
**_`storage LevelUP`_**

```bash section 6
 npm i level
 touch models/notes-level.mjs
 npm run start-level
```

---

### VII section 07

chapter 07  
section 07  
**_`SQL with SQLite3`_**

```bash section 7
npm i sqlite3
touch models/schema-sqlite3.sql
npm run sqlite3-setup
touch models/notes-sqlite3.mjs
npm run start-sqlite3
DEBUG=notez:* npm run start-sqlite3
npm run start-sqlite3
sqlite3 chap07.sqlite3
```

**_`SQL with SQLite3`_**

```sql
select * from notes;
```

---

### VII section 08

chapter 07  
section 08  
**_`ORM way with Sequelize`_**

```bash section 8
npm i sequelize
npm i js-yaml
touch models/notes-sequelize.mjs
touch models/sequelize-sqlite.yaml
```

---

### VII - section 09

chapter 07  
section 09  
**_`MongoDB`_**

```bash section 9
wget -qO - https://www.mongodb.org/static/pgp/server-4.2.asc | sudo apt-key add -
echo "deb [ arch=amd64,arm64 ] https://repo.mongodb.org/apt/ubuntu xenial/mongodb-org/4.2 multiverse" | sudo tee /etc/apt/sources.list.d/mongodb-org-4.2.list
sudo apt-get install -y mongodb-org
which mongo
mongo
echo "mongodb-org hold" | sudo dpkg --set-selections
echo "mongodb-org-server hold" | sudo dpkg --set-selections
echo "mongodb-org-shell hold" | sudo dpkg --set-selections
echo "mongodb-org-mongos hold" | sudo dpkg --set-selections
echo "mongodb-org-tools hold" | sudo dpkg --set-selections
sudo systemctl start mongod
sudo apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv EA312927
echo "deb http://repo.mongodb.org/apt/ubuntu xenial/mongodb-org/3.2 multiverse" | sudo tee /etc/apt/sources.list.d/mongodb-org-3.2.list
sudo apt-get update
sudo apt-get install -y mongodb-org
sudo apt-get purge mongodb-org*
Remove MongoDB
mongo db
sudo apt install mongodb-clients
mongo db
sudo apt-get purge mongodb mongodb-clients mongodb-server mongodb-dev
sudo apt-get purge mongodb-10gen
sudo apt-get autoremove
sudo apt-key adv --keyserver keyserver.ubuntu.com --recv 7F0CEB10
nano /etc/apt/sources.lists
sudo nano /etc/apt/sources.lists
nano /etc/apt/sources.lists
sudo apt-get install mongodb-10gen
sudo rm /var/lib/mongodb/mongod.lock
mongod --repair
sudo apt install mongodb-server-core
sudo service mongodb start
mongo
mongodb
mongod
sudo service mongodb start
mongo
mongod
mongod --repair
which mongod
sudo apt remove mongod
mongodb
sudo rm /var/lib/mongodb/mongod.lock
sudo apt-get purge mongodb-org*
sudo rm -r /var/log/mongodb /var/lib/mongodb
sudo apt-get purge mongod*
mongodb
which mongod
nano /etc/apt/sources.lists
sudo nano /etc/apt/sources.lists
nano /etc/apt/sources.lists
which mongo
mongo
sudo apt install mongodb-clients
mongo
mongodb
sudo apt uninstall mongodb-clients
sudo apt remove mongodb-clients
sudo apt purge mongodb-clients
mongo
which mongo
mongodb
mongod
sudo apt install mongodb-server-core
mongod
sudo apt install mongodb-clients
mongod
which mongo
mongodb
mongod
npm i mongodb
npm audit
touch models/notes-mongodb.mjs

```

---

---

## Chapter 08

---

---

### VIII section 02

chapter 08  
section 02  
**_`user information microservice`_**

```bash section 2
mkdir userz
cd userz
npm init
npm i debug fs-extra js-yaml restify restify-clients sequelize sqlite3
touch users-sequelize.mjs
touch user-server.mjs
touch sequelize-sqlite.yaml
touch users-add.js
touch users-find.js
cd notez
cd ..
cd notez
touch models/users-superagent.mjs
touch routes/users.mjs
touch views/login.hbs

git remote add origin https://github.com/TurtleWolf/HerronNotez.git
git branch c08s02
git checkout c08s02
npm i mysql
npm start
PORT=3333 node users-add.js
cd notez
PORT=3333 node users-add.js
sqlite3 users-sequelize.sqlite3
PORT=3333 node users-find.js me
npm i superagent
npm i passport passport-local
npm i express-session session-file-store
touch views/login.hbs
touch partials/not-logged-in.hbs
cd /Desktop/HerronChapter08/userz
cd ~/Desktop/HerronChapter08/userz
cd notez
ls -l sessions/
npm run start-server2
npm i passport-twitter
ls -al
touch public/assets/vendor/twitter
mkdir public/assets/vendor/twitter
cd public
cd assets
mkdir vendor
cd vendor
mkdir twitter
cd twitter
npm start
```

debug  
fs-extra  
js-yaml  
mysql  
restify  
restify-clients  
sequelize  
sqlite3

---

### VIII section 03

chapter 08  
section 03  
**_`Securely keeping secrets and passwords`_**

---

### VIII section 04

chapter 08  
section 04  
**_`The Notes application stack`_**

---

---

## Chapter 09

---

---

### IX section 02

chapter 09  
section 02  
**_`Socket IO`_**

---

### IX section 03

chapter 09  
section 03  
**_`Socket IO with Express`_**

---

### IX section 04

chapter 09  
section 04  
**_`user information microservice`_**

---

### IX section 05

chapter 09  
section 05  
**_`user information microservice`_**---

---

---

## Chapter 10

---

---

### X section 02

chapter 09  
section 02  
**_`Socket IO`_**

---

### X section 03

chapter 09  
section 03  
**_`Socket IO with Express`_**

---

### X section 04

chapter 09  
section 04  
**_`user information microservice`_**

---

### X section 05

chapter 09  
section 05  
**_`user information microservice`_**---

---

---

## Chapter 11

---

---

### XI section 02

chapter 09  
section 02  
**_`Socket IO`_**

---

### XI section 03

chapter 09  
section 03  
**_`Socket IO with Express`_**

---

### XI section 04

chapter 09  
section 04  
**_`user information microservice`_**

---

### XI section 05

chapter 09  
section 05  
**_`user information microservice`_**

---

---

1. [![alt text](https://github.com/adam-p/markdown-here/raw/master/src/common/images/icon48.png 'Logo Title Text 1')David Herron:](https://www.google.com "Google's Homepage")

1. [![alt text](https://github.com/adam-p/markdown-here/raw/master/src/common/images/icon48.png 'Logo Title Text 1')Andy Harris:](https://www.google.com "Google's Homepage")

1. [![alt text](https://github.com/adam-p/markdown-here/raw/master/src/common/images/icon48.png 'Logo Title Text 1')Dylan Isreal:](https://www.google.com "Google's Homepage")

1. [![alt text](https://github.com/adam-p/markdown-here/raw/master/src/common/images/icon48.png 'Logo Title Text 1')Snow:](https://www.google.com "Google's Homepage")

1. [![alt text](https://github.com/adam-p/markdown-here/raw/master/src/common/images/icon48.png 'Logo Title Text 1')Stephen Meyuex:](https://www.google.com "Google's Homepage")

1. [![alt text](https://github.com/adam-p/markdown-here/raw/master/src/common/images/icon48.png 'Logo Title Text 1')Brad Traversy:](https://www.google.com "Google's Homepage")

1. [![alt text](https://github.com/adam-p/markdown-here/raw/master/src/common/images/icon48.png 'Logo Title Text 1')Maximillian Schwartz:](https://www.google.com "Google's Homepage")

1. [![alt text](https://github.com/adam-p/markdown-here/raw/master/src/common/images/icon48.png 'Logo Title Text 1')Brett Fischer:](https://www.google.com "Google's Homepage")

1. [![alt text](https://github.com/adam-p/markdown-here/raw/master/src/common/images/icon48.png 'Logo Title Text 1')Inline-style:](https://www.google.com "Google's Homepage")

1. [![alt text](https://github.com/adam-p/markdown-here/raw/master/src/common/images/icon48.png 'Logo Title Text 1')Inline-style:](https://www.google.com "Google's Homepage")

chapter 08
section 02
user information microservice

```bash

```
