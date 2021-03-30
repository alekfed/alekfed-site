+++
title = "Databases"
subtitle = "Experience: 3 years"
tags = ['System']
date = 2020-03-25

# For description meta tag
description = "My experience with databases."

# Comment next line and the default banner wil be used.
banner = 'img/databases.svg'

+++

I have an experience with both traditional relational databases and NoSQL.

# RDBMS

I worked with PostgresSQL, MySQL and SQLite. PostgreSQL is a universal option that has some useful features like triggers and can even store JSON. Nevertheless, MySQL was the main database choice for 00s, so I had a chance to work with it as well (including MariaDB). I also used SQLite to collect and store operating information of the test equipment.

Despite the potential of SQL as a DSL, there has not been a need to optimize database queries in my practice yet, in contrast to the abundance of many-to-many relationships in relational schemas. For this reason, my experience is primarily based on interacting with the ORM.

# NoSQL

Among the document-oriented databases, I have the most experience with [MongoDB](https://www.mongodb.com/), to a lesser extent with [CouchDB](https://couchdb.apache.org/) and [ArangoDB](https://www.arangodb.com/). The idea of storing documents as a whole is not a bad idea until there is a need to make batch requests for separate fields of documents in different collections. Even a specialized query DSL (ArangoDB) or  REST-based queries (CouchDB) are not up to the convenience of SQL, so now I have a rather reserved attitude for databases of this type.

Among key-value storages, I used [Redis](https://redis.io/) to store process IDs in the task scheduler and used it as a primitive message queue. It worked well, but at some point [RabbitMQ](https://www.rabbitmq.com/) was deployed.

Among columnar databases, I have a little experience with [HBase](https://hbase.apache.org/) which I planned to use for an analytics task, but then it became clear that a columnar database was not suitable for that particular task, and I didn't return to it anymore.

___
# Illustration

- Composition as a whole: [Dali homage](https://en.wikipedia.org/wiki/The_Elephants).

- Title: [PostgreSQL](https://www.postgresql.org/) logo.

- Monospaced font tables in the "clouds": you begin to perceive the databases themselves in this form after some time working with them from the terminal. There are `\x` in PostgreSQL or `\G` in MySQL however...

- The elephant: [Apache Hadoop](https://hadoop.apache.org/). Unfortunately, I've not come across any tasks that require such a scale.

- Obelist on the elephant's back: [Redis](https://redis.io/).

- Small blue octopus at the feet of the elephant: [ScyllaDB](https://www.scylladb.com/) mascot. It's an interesting project considering its full compatibility with the Cassandra ecosystem. But, as in the case of the latter, I didn't have the opportunity to use it in production.

- "House" in the background: [Memcached](https://memcached.org/). Since functionality of Redis overlaps with that of Memcached, I have a very superficial knowledge of the latter.
