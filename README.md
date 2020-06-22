# Leaves on DataStax Astra™ with NoSQL, and Apache Cassandra™ in the cloud! 

![version](https://img.shields.io/badge/version-0.0.2-blue)

[![Open in Gitpod](https://gitpod.io/button/open-in-gitpod.svg)](https://gitpod.io/#https://github.com/anant/cassandra.api.git)

## Table of Contents

- [Astra Setup & Configuring Credentials](#setup) 
- [Getting Started](#Getting-Started)
	- [Running Data Migrator](#Data-Migrator)
	- Running APIs
		- [Node JS](#Node-js)
		- [Python](#python)
	- [Running Unit Tests](#testing)
  
---

## Setup


1. Before you start using our tools, you'll need to create an account on DataStax Astra:
```
https://astra.datastax.com/register
```

![Astra](Assets/../Assets/Images/astra5.png)

2. You'll then be directed to this screen where you fill in details to launch new Astra Database.

![Astra](Assets/../Assets/Images/astra6.png)

3. Then, you'll need to do on Astra is to download your "secure-connection-details-zip". To do that, click on the actions button in the top left section of the screen then click on "Conection Details"

![Astra](Assets/../Assets/Images/astra7.png)

4. After, click on the link to "Download secure connect bundle" and save the zip file to the **cassandra.api/astra.credentials** directory of this project. 

![Astra](Assets/../Assets/Images/astra8.png)

5. ***Fill in the naming conventions you declared earlier, when you setup your database, in your (cassandra.api/astra.credentials/UserCred.json) file***
- The following is an example of what the UserCred.json would look like following the example in the screenshots above.

```
database name: "KVUser",
keyspace name: "KVPassword",
username: "leavesnetwork",
password: "killrvideo",
table: "leaves"
```

The last value ``table`` wasn't declared before so you can do that here for the first time.

---

## Getting Started

***It's best to go through this project in the following order so you do not get confused.***



### 1. First, run the data migrator to transfer data from our cassandra.api to your Astra Database.

#### [Data Migrator](https://github.com/Anant/cassandra.api/tree/master/astra.import)



### 2. Second, setup an API so that you can communicate with your Astra database. We have 2 APIs for you to use:


#### [Node JS](https://github.com/Anant/cassandra.api/tree/master/astra.api/leaves.api.node)


#### [Python](https://github.com/Anant/cassandra.api/tree/master/astra.api/leaves.api.python)


#### API Reference Material

[Building REST API Blog Post](https://blog.anant.us/building-a-rest-api-with-cassandra-on-datastax-astra-using-python-and-node/)

[Building REST API Webinar Recording](https://www.youtube.com/watch?v=O64pJa3eLqs)



### 3. Third, run this set of unit tests against your API to confirm that it is working properly.

#### [Testing](https://github.com/Anant/cassandra.api/tree/master/astra.api/leaves.api.tests)
