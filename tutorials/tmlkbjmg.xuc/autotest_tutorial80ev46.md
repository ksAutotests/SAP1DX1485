---
title: autotest3kCNX5
description: autotest554K06_10/28/2019 10:03:47 PM
tags: [topic:139269250608756787992873,products:tech/73554900100700000996,tutorial:experience/advanced]
primary_tag: tutorial:product/sapHana
time: 120
author_profile: https://github.com/ksAutotests
author_name: ksAutotests
---
### You will learn
- You will learn this
- and that

autotest tutorial textH82N80

## Prerequisites
- Prerequisute1
- Prerequisute2
- Prerequisute3

[ACCORDION-BEGIN [](176d27ef)]
2bb7c96b-fedb-4261-a9d7-88686cbb197d

[OPTION BEGIN [first]]
```Sql
CREATE KEYSPACE videodb WITH REPLICATION = { 'class' : 'SimpleStrategy', 'replication_factor' : 1 };
use videodb;

// Basic entity table
// Object mapping ?
CREATE TABLE users (
   username varchar,
   firstname varchar,
   lastname varchar,
   email varchar,
   password varchar,
   created_date timestamp,
   total_credits int,
   credit_change_date timeuuid,
   PRIMARY KEY (username)
);

// One-to-many entity table
CREATE TABLE videos (
   videoid uuid,
   videoname varchar,
   username varchar,
   description varchar, 
   tags list<varchar>,
   upload_date timestamp,
   PRIMARY KEY (videoid)
);

// One-to-many from the user point of view
// Also know as a lookup table
CREATE TABLE username_video_index (
   username varchar,
   videoid uuid,
   upload_date timestamp,
   videoname varchar,
   PRIMARY KEY (username, videoid)
);

// Counter table
CREATE TABLE video_rating (
   videoid uuid,
   rating_counter counter,
   rating_total counter,
   PRIMARY KEY (videoid)
);

// Creating index tables for tab keywords
CREATE TABLE tag_index (
   tag varchar, 
   videoid uuid,
   timestamp timestamp,
   PRIMARY KEY (tag, videoid)
);

// Comments as a many-to-many 
// Looking from the video side to many users
CREATE TABLE comments_by_video (
   videoid uuid,
   username varchar,
   comment_ts timestamp,
   comment varchar,
   PRIMARY KEY (videoid,comment_ts,username)
) WITH CLUSTERING ORDER BY (comment_ts DESC, username ASC);
```
[OPTION END]

[ACCORDION-END]

[ACCORDION-BEGIN [](c1f29449)]
[OPTION BEGIN [first]]
```Cds
@AbapCatalog.sqlViewName: 'DEMO_CDS_SESSVAR' 
@AccessControl.authorizationCheck: #NOT_REQUIRED 
define view demo_cds_session_variables 
   as 
   select 
     from demo_expressions 
       { id, 
         $session.user            as system_user, 
         $session.client          as system_client, 
         $session.system_language as system_language     
        }
```
[OPTION END]

[OPTION BEGIN [second]]
66b47814

[OPTION END]

[ACCORDION-END]

[ACCORDION-BEGIN [](bfd3e498)]
[OPTION BEGIN [first]]
```Cds
@AbapCatalog.sqlViewName: 'DEMO_CDS_SESSVAR' 
@AccessControl.authorizationCheck: #NOT_REQUIRED 
define view demo_cds_session_variables 
   as 
   select 
     from demo_expressions 
       { id, 
         $session.user            as system_user, 
         $session.client          as system_client, 
         $session.system_language as system_language     
        }
```
[OPTION END]

[OPTION BEGIN [second]]
51b31a46

[OPTION END]

[OPTION BEGIN [third]]
![image](https://www.sap.com/favicon.ico)
[OPTION END]

[ACCORDION-END]

