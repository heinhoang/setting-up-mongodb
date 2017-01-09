# Setting Up MongoDB
A little hint to settup mongoDB

1. Install MongoDB on your machine
2. Clone this package into your drive such as 'D:'
3. Open Terminal & setting up mongoDB (more at [stackoverflow](http://stackoverflow.com/questions/2404742/how-to-install-mongodb-on-windows) or at [mongo website](https://docs.mongodb.com/manual/reference/configuration-options/))
```
$ "C:\Program Files\MongoDB\Server\3.4\bin\mongod.exe" --directoryperdb --install
# setting configs
$ "C:\Program Files\MongoDB\Server\3.4\bin\mongod.exe" --config "D:\mongo\etc\mongo.cfg"
# connect to MongoDB
$ "C:\Program Files\MongoDB\Server\3.4\bin\mongod.exe"
$ "C:\Program Files\MongoDB\Server\3.4\bin\mongo.exe"
```
4. If meet error `initAndListen: 28663 Cannot start server` ([know more here](http://stackoverflow.com/questions/34243731/mongodb-cannot-start-server-the-default-storage-engine-wiredtiger-is-not-avai))
```
$ "C:\Program Files\MongoDB\Server\3.4\bin\mongod.exe" --storageEngine=mmapv1 --config "D:\mongo\etc\mongo.cfg"
```