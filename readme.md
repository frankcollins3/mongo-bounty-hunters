➜  ~ cd desktop[
zsh: bad pattern: desktop[
➜  ~ cd desktop
➜  desktop git clone https://github.com/frankcollins3/mongo-bounty-hunters.git
Cloning into 'mongo-bounty-hunters'...
remote: Enumerating objects: 43, done.
remote: Counting objects: 100% (43/43), done.
remote: Compressing objects: 100% (22/22), done.
remote: Total 43 (delta 18), reused 43 (delta 18), pack-reused 0
Unpacking objects: 100% (43/43), done.
➜  desktop cd mongo-bounty-hunters
➜  mongo-bounty-hunters git:(main) mongo
MongoDB shell version v4.4.1
connecting to: mongodb://127.0.0.1:27017/?compressors=disabled&gssapiServiceName=mongodb
Implicit session: session { "id" : UUID("9a8d328d-7170-436e-81b9-f9d5ce008148") }
MongoDB server version: 4.4.1
---
The server generated these startup warnings when booting:
        2020-12-14T10:45:26.922-05:00: Access control is not enabled for the database. Read and write access to data and configuration is unrestricted
        2020-12-14T10:45:26.922-05:00: Soft rlimits too low
        2020-12-14T10:45:26.922-05:00:         currentValue: 256
        2020-12-14T10:45:26.922-05:00:         recommendedMinimum: 64000
---
---
        Enable MongoDB's free cloud-based monitoring service, which will then receive and display
        metrics about your deployment (disk utilization, CPU, operation statistics, etc).

        The monitoring data will be available on a MongoDB website with a unique URL accessible to you
        and anyone you share the URL with. MongoDB may use this information to make product
        improvements and to suggest MongoDB products and deployment options to you.

        To enable free monitoring, run the following command: db.enableFreeMonitoring()
        To permanently disable this reminder, run the following command: db.disableFreeMonitoring()
---
> views hunters
uncaught exception: SyntaxError: unexpected token: identifier :
@(shell):1:6
> use hunters
switched to db hunters
> db.createCollection('bounties')
{ "ok" : 1 }
> db.bounties.insert(
...   {
...     name: 'Han Solo',
...     wantedFor : 'Owing money',
...     client : 'Jabba the Hut',
...     reward : 1000000,
...     ship: 'Millennium Falcon',
...     hunters :['Bobba Fett', 'Dengar', 'IG-88', 'Zuckuss', 'Greedo', 'Bossk', '4-LOM'],
...     captured: false
...   }
...   )
WriteResult({ "nInserted" : 1 })
> db.bounties.insert([
...   {
...     name: 'Han Solo',
...     wantedFor : 'Owing money',
...     client : 'Jabba the Hut',
...     reward : 1000000,
...     ship: 'Millennium Falcon',
...     hunters :['Bobba Fett', 'Dengar', 'IG-88', 'Zuckuss', 'Greedo', 'Bossk', '4-LOM'],
...     captured: false
...   },
...   {
...     name: 'Rocket',
...     wantedFor : 'Stealing Batteries',
...     client : 'Ayesha High Priestess of the Sovereign',
...     reward : 1000000000,
...     ship: 'The Milano',
...     hunters :['Nebula', 'Ravagers'],
...     captured: false
...   },
...   {
...     name: 'Sara Lance',
...     wantedFor : 'Screwing up the timeline, causing anachronisms',
...     client : 'Time Bureau',
...     reward : 50000,
...     ship: 'Waverider',
...     hunters :['Chronos'],
...     captured: false
...   },
...   {
...     name: 'Malcolm Reynolds',
...     wantedFor : 'Aiming to misbehave',
...     client : 'The Alliance',
...     reward : 40000,
...     ship: 'Serenity',
...     hunters :['Jubal Early'],
...     captured: false
...   },
...   {
...     name: 'Starbuck',
...     wantedFor : "Disobeying Captain's orders",
...     client : 'Captain Adama',
...     ship: 'Demetrius',
...     reward : 1000,
...     hunters :['Apollo'],
...     captured: true
...   }
... ])
BulkWriteResult({
	"writeErrors" : [ ],
	"writeConcernErrors" : [ ],
	"nInserted" : 5,
	"nUpserted" : 0,
	"nMatched" : 0,
	"nModified" : 0,
	"nRemoved" : 0,
	"upserted" : [ ]
})
> db.getCollectionnames()
uncaught exception: TypeError: db.getCollectionnames is not a function :
@(shell):1:1
> db.getCollectionNames()
[ "bounties" ]
> db.people.find({name: 'Starbuck'})
> mongo
uncaught exception: ReferenceError: mongo is not defined :
@(shell):1:1
> mongo
uncaught exception: ReferenceError: mongo is not defined :
@(shell):1:1
> db.people.find()
> ^C
bye
➜  mongo-bounty-hunters git:(main) mongo
MongoDB shell version v4.4.1
connecting to: mongodb://127.0.0.1:27017/?compressors=disabled&gssapiServiceName=mongodb
Implicit session: session { "id" : UUID("d646e5aa-98d5-4ead-afe5-29a8d481c43d") }
MongoDB server version: 4.4.1
---
The server generated these startup warnings when booting:
        2020-12-14T10:45:26.922-05:00: Access control is not enabled for the database. Read and write access to data and configuration is unrestricted
        2020-12-14T10:45:26.922-05:00: Soft rlimits too low
        2020-12-14T10:45:26.922-05:00:         currentValue: 256
        2020-12-14T10:45:26.922-05:00:         recommendedMinimum: 64000
---
---
        Enable MongoDB's free cloud-based monitoring service, which will then receive and display
        metrics about your deployment (disk utilization, CPU, operation statistics, etc).

        The monitoring data will be available on a MongoDB website with a unique URL accessible to you
        and anyone you share the URL with. MongoDB may use this information to make product
        improvements and to suggest MongoDB products and deployment options to you.

        To enable free monitoring, run the following command: db.enableFreeMonitoring()
        To permanently disable this reminder, run the following command: db.disableFreeMonitoring()
---
> db.bounties
test.bounties
> db.bounties.find()
> ^C
bye
➜  mongo-bounty-hunters git:(main) use bounties
zsh: command not found: use
➜  mongo-bounty-hunters git:(main) mongo
MongoDB shell version v4.4.1
uconnecting to: mongodb://127.0.0.1:27017/?compressors=disabled&gssapiServiceName=mongodb
Implicit session: session { "id" : UUID("838a5cc8-669d-48f2-9327-eca4c7511a04") }
MongoDB server version: 4.4.1
---
The server generated these startup warnings when booting:
        2020-12-14T10:45:26.922-05:00: Access control is not enabled for the database. Read and write access to data and configuration is unrestricted
        2020-12-14T10:45:26.922-05:00: Soft rlimits too low
        2020-12-14T10:45:26.922-05:00:         currentValue: 256
        2020-12-14T10:45:26.922-05:00:         recommendedMinimum: 64000
---
---
        Enable MongoDB's free cloud-based monitoring service, which will then receive and display
        metrics about your deployment (disk utilization, CPU, operation statistics, etc).

        The monitoring data will be available on a MongoDB website with a unique URL accessible to you
        and anyone you share the URL with. MongoDB may use this information to make product
        improvements and to suggest MongoDB products and deployment options to you.

        To enable free monitoring, run the following command: db.enableFreeMonitoring()
        To permanently disable this reminder, run the following command: db.disableFreeMonitoring()
---
> use bounties
switched to db bounties
> db.bounties.find()
> db.getCollectionNames()
[ ]
> ^C
bye
➜  mongo-bounty-hunters git:(main) mongo
MongoDB shell version v4.4.1
uconnecting to: mongodb://127.0.0.1:27017/?compressors=disabled&gssapiServiceName=mongodb
Implicit session: session { "id" : UUID("039489dc-8cba-489e-9b97-4032fe35c851") }
MongoDB server version: 4.4.1
---
The server generated these startup warnings when booting:
        2020-12-14T10:45:26.922-05:00: Access control is not enabled for the database. Read and write access to data and configuration is unrestricted
        2020-12-14T10:45:26.922-05:00: Soft rlimits too low
        2020-12-14T10:45:26.922-05:00:         currentValue: 256
        2020-12-14T10:45:26.922-05:00:         recommendedMinimum: 64000
---
---
        Enable MongoDB's free cloud-based monitoring service, which will then receive and display
        metrics about your deployment (disk utilization, CPU, operation statistics, etc).

        The monitoring data will be available on a MongoDB website with a unique URL accessible to you
        and anyone you share the URL with. MongoDB may use this information to make product
        improvements and to suggest MongoDB products and deployment options to you.

        To enable free monitoring, run the following command: db.enableFreeMonitoring()
        To permanently disable this reminder, run the following command: db.disableFreeMonitoring()
---
> use hunters
switched to db hunters
> db.collectionsName()
uncaught exception: TypeError: db.collectionsName is not a function :
@(shell):1:1
> db.getCollectionNames()
[ "bounties" ]
> db.bounties.find()
{ "_id" : ObjectId("5fd7a36db85f58d79df14b5b"), "name" : "Han Solo", "wantedFor" : "Owing money", "client" : "Jabba the Hut", "reward" : 1000000, "ship" : "Millennium Falcon", "hunters" : [ "Bobba Fett", "Dengar", "IG-88", "Zuckuss", "Greedo", "Bossk", "4-LOM" ], "captured" : false }
{ "_id" : ObjectId("5fd7a398b85f58d79df14b5c"), "name" : "Han Solo", "wantedFor" : "Owing money", "client" : "Jabba the Hut", "reward" : 1000000, "ship" : "Millennium Falcon", "hunters" : [ "Bobba Fett", "Dengar", "IG-88", "Zuckuss", "Greedo", "Bossk", "4-LOM" ], "captured" : false }
{ "_id" : ObjectId("5fd7a398b85f58d79df14b5d"), "name" : "Rocket", "wantedFor" : "Stealing Batteries", "client" : "Ayesha High Priestess of the Sovereign", "reward" : 1000000000, "ship" : "The Milano", "hunters" : [ "Nebula", "Ravagers" ], "captured" : false }
{ "_id" : ObjectId("5fd7a398b85f58d79df14b5e"), "name" : "Sara Lance", "wantedFor" : "Screwing up the timeline, causing anachronisms", "client" : "Time Bureau", "reward" : 50000, "ship" : "Waverider", "hunters" : [ "Chronos" ], "captured" : false }
{ "_id" : ObjectId("5fd7a398b85f58d79df14b5f"), "name" : "Malcolm Reynolds", "wantedFor" : "Aiming to misbehave", "client" : "The Alliance", "reward" : 40000, "ship" : "Serenity", "hunters" : [ "Jubal Early" ], "captured" : false }
{ "_id" : ObjectId("5fd7a398b85f58d79df14b60"), "name" : "Starbuck", "wantedFor" : "Disobeying Captain's orders", "client" : "Captain Adama", "ship" : "Demetrius", "reward" : 1000, "hunters" : [ "Apollo" ], "captured" : true }
> db.bounties.find({client: 'Time Bureau'})
{ "_id" : ObjectId("5fd7a398b85f58d79df14b5e"), "name" : "Sara Lance", "wantedFor" : "Screwing up the timeline, causing anachronisms", "client" : "Time Bureau", "reward" : 50000, "ship" : "Waverider", "hunters" : [ "Chronos" ], "captured" : false }
> db.bounties.find({captured: true})
{ "_id" : ObjectId("5fd7a398b85f58d79df14b60"), "name" : "Starbuck", "wantedFor" : "Disobeying Captain's orders", "client" : "Captain Adama", "ship" : "Demetrius", "reward" : 1000, "hunters" : [ "Apollo" ], "captured" : true }
> db.bounties.find({}, { name: true, _id: false })
{ "name" : "Han Solo" }
{ "name" : "Han Solo" }
{ "name" : "Rocket" }
{ "name" : "Sara Lance" }
{ "name" : "Malcolm Reynolds" }
{ "name" : "Starbuck" }
> db.bounties.remove({name: 'Starbuck'})
WriteResult({ "nRemoved" : 1 })
> db.bounties.remove({_id : ObjectId("5fd7a398b85f58d79df14b5c"})
... mongo
...
...
>
> db.bunties.remove({_id : ObjectId("5fd7a398b85f58d79df14b5c")})
WriteResult({ "nRemoved" : 0 })
> db.bounties.find()
{ "_id" : ObjectId("5fd7a36db85f58d79df14b5b"), "name" : "Han Solo", "wantedFor" : "Owing money", "client" : "Jabba the Hut", "reward" : 1000000, "ship" : "Millennium Falcon", "hunters" : [ "Bobba Fett", "Dengar", "IG-88", "Zuckuss", "Greedo", "Bossk", "4-LOM" ], "captured" : false }
{ "_id" : ObjectId("5fd7a398b85f58d79df14b5c"), "name" : "Han Solo", "wantedFor" : "Owing money", "client" : "Jabba the Hut", "reward" : 1000000, "ship" : "Millennium Falcon", "hunters" : [ "Bobba Fett", "Dengar", "IG-88", "Zuckuss", "Greedo", "Bossk", "4-LOM" ], "captured" : false }
{ "_id" : ObjectId("5fd7a398b85f58d79df14b5d"), "name" : "Rocket", "wantedFor" : "Stealing Batteries", "client" : "Ayesha High Priestess of the Sovereign", "reward" : 1000000000, "ship" : "The Milano", "hunters" : [ "Nebula", "Ravagers" ], "captured" : false }
{ "_id" : ObjectId("5fd7a398b85f58d79df14b5e"), "name" : "Sara Lance", "wantedFor" : "Screwing up the timeline, causing anachronisms", "client" : "Time Bureau", "reward" : 50000, "ship" : "Waverider", "hunters" : [ "Chronos" ], "captured" : false }
{ "_id" : ObjectId("5fd7a398b85f58d79df14b5f"), "name" : "Malcolm Reynolds", "wantedFor" : "Aiming to misbehave", "client" : "The Alliance", "reward" : 40000, "ship" : "Serenity", "hunters" : [ "Jubal Early" ], "captured" : false }
> db.bounties.update({name: 'Sara Lance'}, {$set: {name: 'White Canary'}})
WriteResult({ "nMatched" : 1, "nUpserted" : 0, "nModified" : 1 })
> db.bounties.update({name: 'Rocket'}, {$set {ship: 'The Milano 2'}})
uncaught exception: SyntaxError: missing : after property id :
@(shell):1:43
> db.bountiesupdate({name: 'Rocket', {$set: {ship: The Milano 2}})
...
...
>
> db.bounties.update({name: 'Rocket', {$set: {ship: "The Milano 2"}})
...
...
>
> mongo
uncaught exception: ReferenceError: mongo is not defined :
@(shell):1:1
> db.bounties.find()
{ "_id" : ObjectId("5fd7a36db85f58d79df14b5b"), "name" : "Han Solo", "wantedFor" : "Owing money", "client" : "Jabba the Hut", "reward" : 1000000, "ship" : "Millennium Falcon", "hunters" : [ "Bobba Fett", "Dengar", "IG-88", "Zuckuss", "Greedo", "Bossk", "4-LOM" ], "captured" : false }
{ "_id" : ObjectId("5fd7a398b85f58d79df14b5c"), "name" : "Han Solo", "wantedFor" : "Owing money", "client" : "Jabba the Hut", "reward" : 1000000, "ship" : "Millennium Falcon", "hunters" : [ "Bobba Fett", "Dengar", "IG-88", "Zuckuss", "Greedo", "Bossk", "4-LOM" ], "captured" : false }
{ "_id" : ObjectId("5fd7a398b85f58d79df14b5d"), "name" : "Rocket", "wantedFor" : "Stealing Batteries", "client" : "Ayesha High Priestess of the Sovereign", "reward" : 1000000000, "ship" : "The Milano", "hunters" : [ "Nebula", "Ravagers" ], "captured" : false }
{ "_id" : ObjectId("5fd7a398b85f58d79df14b5e"), "name" : "White Canary", "wantedFor" : "Screwing up the timeline, causing anachronisms", "client" : "Time Bureau", "reward" : 50000, "ship" : "Waverider", "hunters" : [ "Chronos" ], "captured" : false }
{ "_id" : ObjectId("5fd7a398b85f58d79df14b5f"), "name" : "Malcolm Reynolds", "wantedFor" : "Aiming to misbehave", "client" : "The Alliance", "reward" : 40000, "ship" : "Serenity", "hunters" : [ "Jubal Early" ], "captured" : false }
> db.bounties.find{(:name: "Malcolm Reynolds"})
uncaught exception: SyntaxError: unexpected token: '{' :
@(shell):1:16
> show dbs
admin         0.000GB
config        0.000GB
hunters       0.000GB
introToMongo  0.000GB
local         0.000GB
myDB          0.000GB
people        0.000GB
> use introToMongo
switched to db introToMongo
> db.dropDatabase()
{ "dropped" : "introToMongo", "ok" : 1 }
> show dbs
admin    0.000GB
config   0.000GB
hunters  0.000GB
local    0.000GB
myDB     0.000GB
people   0.000GB
> use people
switched to db people
> db.dropDatabase()
{ "dropped" : "people", "ok" : 1 }
> show dbs
admin    0.000GB
config   0.000GB
hunters  0.000GB
local    0.000GB
myDB     0.000GB
> use myDB
switched to db myDB
> db.dropDatabase()
{ "dropped" : "myDB", "ok" : 1 }
> use hunters
switched to db hunters
> show collections
bounties
> db.hunters.find()
> db.bounties.find()
{ "_id" : ObjectId("5fd7a36db85f58d79df14b5b"), "name" : "Han Solo", "wantedFor" : "Owing money", "client" : "Jabba the Hut", "reward" : 1000000, "ship" : "Millennium Falcon", "hunters" : [ "Bobba Fett", "Dengar", "IG-88", "Zuckuss", "Greedo", "Bossk", "4-LOM" ], "captured" : false }
{ "_id" : ObjectId("5fd7a398b85f58d79df14b5c"), "name" : "Han Solo", "wantedFor" : "Owing money", "client" : "Jabba the Hut", "reward" : 1000000, "ship" : "Millennium Falcon", "hunters" : [ "Bobba Fett", "Dengar", "IG-88", "Zuckuss", "Greedo", "Bossk", "4-LOM" ], "captured" : false }
{ "_id" : ObjectId("5fd7a398b85f58d79df14b5d"), "name" : "Rocket", "wantedFor" : "Stealing Batteries", "client" : "Ayesha High Priestess of the Sovereign", "reward" : 1000000000, "ship" : "The Milano", "hunters" : [ "Nebula", "Ravagers" ], "captured" : false }
{ "_id" : ObjectId("5fd7a398b85f58d79df14b5e"), "name" : "White Canary", "wantedFor" : "Screwing up the timeline, causing anachronisms", "client" : "Time Bureau", "reward" : 50000, "ship" : "Waverider", "hunters" : [ "Chronos" ], "captured" : false }
{ "_id" : ObjectId("5fd7a398b85f58d79df14b5f"), "name" : "Malcolm Reynolds", "wantedFor" : "Aiming to misbehave", "client" : "The Alliance", "reward" : 40000, "ship" : "Serenity", "hunters" : [ "Jubal Early" ], "captured" : false }
> db.bounties.update({name : 'Rocket'}, {$set : {ship: 'The Milano 2'}})
WriteResult({ "nMatched" : 1, "nUpserted" : 0, "nModified" : 1 })
> db.bounties.find({reward: {$gt: 10000}})
{ "_id" : ObjectId("5fd7a36db85f58d79df14b5b"), "name" : "Han Solo", "wantedFor" : "Owing money", "client" : "Jabba the Hut", "reward" : 1000000, "ship" : "Millennium Falcon", "hunters" : [ "Bobba Fett", "Dengar", "IG-88", "Zuckuss", "Greedo", "Bossk", "4-LOM" ], "captured" : false }
{ "_id" : ObjectId("5fd7a398b85f58d79df14b5c"), "name" : "Han Solo", "wantedFor" : "Owing money", "client" : "Jabba the Hut", "reward" : 1000000, "ship" : "Millennium Falcon", "hunters" : [ "Bobba Fett", "Dengar", "IG-88", "Zuckuss", "Greedo", "Bossk", "4-LOM" ], "captured" : false }
{ "_id" : ObjectId("5fd7a398b85f58d79df14b5d"), "name" : "Rocket", "wantedFor" : "Stealing Batteries", "client" : "Ayesha High Priestess of the Sovereign", "reward" : 1000000000, "ship" : "The Milano 2", "hunters" : [ "Nebula", "Ravagers" ], "captured" : false }
{ "_id" : ObjectId("5fd7a398b85f58d79df14b5e"), "name" : "White Canary", "wantedFor" : "Screwing up the timeline, causing anachronisms", "client" : "Time Bureau", "reward" : 50000, "ship" : "Waverider", "hunters" : [ "Chronos" ], "captured" : false }
{ "_id" : ObjectId("5fd7a398b85f58d79df14b5f"), "name" : "Malcolm Reynolds", "wantedFor" : "Aiming to misbehave", "client" : "The Alliance", "reward" : 40000, "ship" : "Serenity", "hunters" : [ "Jubal Early" ], "captured" : false }
> db.bounties.find({reward {$lt: 1000}})
uncaught exception: SyntaxError: missing : after property id :
@(shell):1:25
> db.bounties.find({reward: {$lt: 1000}})
> db.bounties.find({reward: { $lt: 1000}})
> db.bounties.find({reward: {$lt: 1000}})
>
>
>
> ^C
bye
➜  mongo-bounty-hunters git:(main) mongo
MongoDB shell version v4.4.1
connecting to: mongodb://127.0.0.1:27017/?compressors=disabled&gssapiServiceName=mongodb
Implicit session: session { "id" : UUID("40aeb6ed-3973-47e3-9a79-6ee8da562a8e") }
MongoDB server version: 4.4.1
---
The server generated these startup warnings when booting:
        2020-12-14T10:45:26.922-05:00: Access control is not enabled for the database. Read and write access to data and configuration is unrestricted
        2020-12-14T10:45:26.922-05:00: Soft rlimits too low
        2020-12-14T10:45:26.922-05:00:         currentValue: 256
        2020-12-14T10:45:26.922-05:00:         recommendedMinimum: 64000
---
---
        Enable MongoDB's free cloud-based monitoring service, which will then receive and display
        metrics about your deployment (disk utilization, CPU, operation statistics, etc).

        The monitoring data will be available on a MongoDB website with a unique URL accessible to you
        and anyone you share the URL with. MongoDB may use this information to make product
        improvements and to suggest MongoDB products and deployment options to you.

        To enable free monitoring, run the following command: db.enableFreeMonitoring()
        To permanently disable this reminder, run the following command: db.disableFreeMonitoring()
---
> show dbs
admin    0.000GB
config   0.000GB
hunters  0.000GB
local    0.000GB
> use hunters
switched to db hunters
> show collections
bounties
> db.bounties.find()
{ "_id" : ObjectId("5fd7a36db85f58d79df14b5b"), "name" : "Han Solo", "wantedFor" : "Owing money", "client" : "Jabba the Hut", "reward" : 1000000, "ship" : "Millennium Falcon", "hunters" : [ "Bobba Fett", "Dengar", "IG-88", "Zuckuss", "Greedo", "Bossk", "4-LOM" ], "captured" : false }
{ "_id" : ObjectId("5fd7a398b85f58d79df14b5c"), "name" : "Han Solo", "wantedFor" : "Owing money", "client" : "Jabba the Hut", "reward" : 1000000, "ship" : "Millennium Falcon", "hunters" : [ "Bobba Fett", "Dengar", "IG-88", "Zuckuss", "Greedo", "Bossk", "4-LOM" ], "captured" : false }
{ "_id" : ObjectId("5fd7a398b85f58d79df14b5d"), "name" : "Rocket", "wantedFor" : "Stealing Batteries", "client" : "Ayesha High Priestess of the Sovereign", "reward" : 1000000000, "ship" : "The Milano 2", "hunters" : [ "Nebula", "Ravagers" ], "captured" : false }
{ "_id" : ObjectId("5fd7a398b85f58d79df14b5e"), "name" : "White Canary", "wantedFor" : "Screwing up the timeline, causing anachronisms", "client" : "Time Bureau", "reward" : 50000, "ship" : "Waverider", "hunters" : [ "Chronos" ], "captured" : false }
{ "_id" : ObjectId("5fd7a398b85f58d79df14b5f"), "name" : "Malcolm Reynolds", "wantedFor" : "Aiming to misbehave", "client" : "The Alliance", "reward" : 40000, "ship" : "Serenity", "hunters" : [ "Jubal Early" ], "captured" : false }
> db.bounties.find({reward: {$lte: 1000}})
> db.bounties.find()
{ "_id" : ObjectId("5fd7a36db85f58d79df14b5b"), "name" : "Han Solo", "wantedFor" : "Owing money", "client" : "Jabba the Hut", "reward" : 1000000, "ship" : "Millennium Falcon", "hunters" : [ "Bobba Fett", "Dengar", "IG-88", "Zuckuss", "Greedo", "Bossk", "4-LOM" ], "captured" : false }
{ "_id" : ObjectId("5fd7a398b85f58d79df14b5c"), "name" : "Han Solo", "wantedFor" : "Owing money", "client" : "Jabba the Hut", "reward" : 1000000, "ship" : "Millennium Falcon", "hunters" : [ "Bobba Fett", "Dengar", "IG-88", "Zuckuss", "Greedo", "Bossk", "4-LOM" ], "captured" : false }
{ "_id" : ObjectId("5fd7a398b85f58d79df14b5d"), "name" : "Rocket", "wantedFor" : "Stealing Batteries", "client" : "Ayesha High Priestess of the Sovereign", "reward" : 1000000000, "ship" : "The Milano 2", "hunters" : [ "Nebula", "Ravagers" ], "captured" : false }
{ "_id" : ObjectId("5fd7a398b85f58d79df14b5e"), "name" : "White Canary", "wantedFor" : "Screwing up the timeline, causing anachronisms", "client" : "Time Bureau", "reward" : 50000, "ship" : "Waverider", "hunters" : [ "Chronos" ], "captured" : false }
{ "_id" : ObjectId("5fd7a398b85f58d79df14b5f"), "name" : "Malcolm Reynolds", "wantedFor" : "Aiming to misbehave", "client" : "The Alliance", "reward" : 40000, "ship" : "Serenity", "hunters" : [ "Jubal Early" ], "captured" : false }
> db.bounties.remove{(_id: ObjectId("5fd7a398b85f58d79df14b5c")})
uncaught exception: SyntaxError: unexpected token: '{' :
@(shell):1:18
> db.bounties.find({name: 'Nebula'})
>
>
> db.bounties.find()
{ "_id" : ObjectId("5fd7a36db85f58d79df14b5b"), "name" : "Han Solo", "wantedFor" : "Owing money", "client" : "Jabba the Hut", "reward" : 1000000, "ship" : "Millennium Falcon", "hunters" : [ "Bobba Fett", "Dengar", "IG-88", "Zuckuss", "Greedo", "Bossk", "4-LOM" ], "captured" : false }
{ "_id" : ObjectId("5fd7a398b85f58d79df14b5c"), "name" : "Han Solo", "wantedFor" : "Owing money", "client" : "Jabba the Hut", "reward" : 1000000, "ship" : "Millennium Falcon", "hunters" : [ "Bobba Fett", "Dengar", "IG-88", "Zuckuss", "Greedo", "Bossk", "4-LOM" ], "captured" : false }
{ "_id" : ObjectId("5fd7a398b85f58d79df14b5d"), "name" : "Rocket", "wantedFor" : "Stealing Batteries", "client" : "Ayesha High Priestess of the Sovereign", "reward" : 1000000000, "ship" : "The Milano 2", "hunters" : [ "Nebula", "Ravagers" ], "captured" : false }
{ "_id" : ObjectId("5fd7a398b85f58d79df14b5e"), "name" : "White Canary", "wantedFor" : "Screwing up the timeline, causing anachronisms", "client" : "Time Bureau", "reward" : 50000, "ship" : "Waverider", "hunters" : [ "Chronos" ], "captured" : false }
{ "_id" : ObjectId("5fd7a398b85f58d79df14b5f"), "name" : "Malcolm Reynolds", "wantedFor" : "Aiming to misbehave", "client" : "The Alliance", "reward" : 40000, "ship" : "Serenity", "hunters" : [ "Jubal Early" ], "captured" : false }
> db.bounties.find({hunter: 'Nebula'})
> db.bounties.find({hunters: 'Nebula'})
{ "_id" : ObjectId("5fd7a398b85f58d79df14b5d"), "name" : "Rocket", "wantedFor" : "Stealing Batteries", "client" : "Ayesha High Priestess of the Sovereign", "reward" : 1000000000, "ship" : "The Milano 2", "hunters" : [ "Nebula", "Ravagers" ], "captured" : false }
> db.bounties.find({ship: 'Waverider', || ship: 'Serenity'})
uncaught exception: SyntaxError: expected property name, got '||' :
@(shell):1:37
> db.bounties.find({ $or: [ {ship: 'Waverider'}, {ship: 'Serenity'} ] } )
{ "_id" : ObjectId("5fd7a398b85f58d79df14b5e"), "name" : "White Canary", "wantedFor" : "Screwing up the timeline, causing anachronisms", "client" : "Time Bureau", "reward" : 50000, "ship" : "Waverider", "hunters" : [ "Chronos" ], "captured" : false }
{ "_id" : ObjectId("5fd7a398b85f58d79df14b5f"), "name" : "Malcolm Reynolds", "wantedFor" : "Aiming to misbehave", "client" : "The Alliance", "reward" : 40000, "ship" : "Serenity", "hunters" : [ "Jubal Early" ], "captured" : false }
> db.bounties.find({ $and: [ {captured: false}, {client: 'Ayesha High Priestess of the Sovereign'} ] })
{ "_id" : ObjectId("5fd7a398b85f58d79df14b5d"), "name" : "Rocket", "wantedFor" : "Stealing Batteries", "client" : "Ayesha High Priestess of the Sovereign", "reward" : 1000000000, "ship" : "The Milano 2", "hunters" : [ "Nebula", "Ravagers" ], "captured" : false }
> db.bounties.updateMany({ {}, $inc: {reward: 33333 }})
uncaught exception: SyntaxError: expected property name, got '{' :
@(shell):1:25
> db.hunters.updateMany({ {}, {$inc: {reward:33333 }})
...
...
> db.hunters.updateMany({ {}, {inc: {reward:33333 }})
... db.bounties.updateMany({ {}, {$inc: {reward:33333 }})
... db.bounties.find()
... mongo
...
...
>
> mongo
uncaught exception: ReferenceError: mongo is not defined :
@(shell):1:1
> db
hunters
> db.bounties.find()
{ "_id" : ObjectId("5fd7a36db85f58d79df14b5b"), "name" : "Han Solo", "wantedFor" : "Owing money", "client" : "Jabba the Hut", "reward" : 1000000, "ship" : "Millennium Falcon", "hunters" : [ "Bobba Fett", "Dengar", "IG-88", "Zuckuss", "Greedo", "Bossk", "4-LOM" ], "captured" : false }
{ "_id" : ObjectId("5fd7a398b85f58d79df14b5c"), "name" : "Han Solo", "wantedFor" : "Owing money", "client" : "Jabba the Hut", "reward" : 1000000, "ship" : "Millennium Falcon", "hunters" : [ "Bobba Fett", "Dengar", "IG-88", "Zuckuss", "Greedo", "Bossk", "4-LOM" ], "captured" : false }
{ "_id" : ObjectId("5fd7a398b85f58d79df14b5d"), "name" : "Rocket", "wantedFor" : "Stealing Batteries", "client" : "Ayesha High Priestess of the Sovereign", "reward" : 1000000000, "ship" : "The Milano 2", "hunters" : [ "Nebula", "Ravagers" ], "captured" : false }
{ "_id" : ObjectId("5fd7a398b85f58d79df14b5e"), "name" : "White Canary", "wantedFor" : "Screwing up the timeline, causing anachronisms", "client" : "Time Bureau", "reward" : 50000, "ship" : "Waverider", "hunters" : [ "Chronos" ], "captured" : false }
{ "_id" : ObjectId("5fd7a398b85f58d79df14b5f"), "name" : "Malcolm Reynolds", "wantedFor" : "Aiming to misbehave", "client" : "The Alliance", "reward" : 40000, "ship" : "Serenity", "hunters" : [ "Jubal Early" ], "captured" : false }
> db.hunters.updateMany({ {}, {$inc: {reward:33333 }})
...
...
>
> db.bounties.update({name: "Malcolm Reynolds"}, {$push: {hunters: "Boba Fett"}})
WriteResult({ "nMatched" : 1, "nUpserted" : 0, "nModified" : 1 })
> db.bounties.find()
{ "_id" : ObjectId("5fd7a36db85f58d79df14b5b"), "name" : "Han Solo", "wantedFor" : "Owing money", "client" : "Jabba the Hut", "reward" : 1000000, "ship" : "Millennium Falcon", "hunters" : [ "Bobba Fett", "Dengar", "IG-88", "Zuckuss", "Greedo", "Bossk", "4-LOM" ], "captured" : false }
{ "_id" : ObjectId("5fd7a398b85f58d79df14b5c"), "name" : "Han Solo", "wantedFor" : "Owing money", "client" : "Jabba the Hut", "reward" : 1000000, "ship" : "Millennium Falcon", "hunters" : [ "Bobba Fett", "Dengar", "IG-88", "Zuckuss", "Greedo", "Bossk", "4-LOM" ], "captured" : false }
{ "_id" : ObjectId("5fd7a398b85f58d79df14b5d"), "name" : "Rocket", "wantedFor" : "Stealing Batteries", "client" : "Ayesha High Priestess of the Sovereign", "reward" : 1000000000, "ship" : "The Milano 2", "hunters" : [ "Nebula", "Ravagers" ], "captured" : false }
{ "_id" : ObjectId("5fd7a398b85f58d79df14b5e"), "name" : "White Canary", "wantedFor" : "Screwing up the timeline, causing anachronisms", "client" : "Time Bureau", "reward" : 50000, "ship" : "Waverider", "hunters" : [ "Chronos" ], "captured" : false }
{ "_id" : ObjectId("5fd7a398b85f58d79df14b5f"), "name" : "Malcolm Reynolds", "wantedFor" : "Aiming to misbehave", "client" : "The Alliance", "reward" : 40000, "ship" : "Serenity", "hunters" : [ "Jubal Early", "Boba Fett" ], "captured" : false }
> db.bounties.update({ $multiply [