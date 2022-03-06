---
title: autotest5a5B2c
description: autotestif0437_3/6/2022 12:38:55 PM
tags: [82352407468693968798155:325f896d-bad5-49ee-a4e6-518589778cd8/139269250608756787992873,197f4ec4-6c14-5b5e-9fb3-058e21403d41:tech/73554900100700000996,c1a376dd-ebd0-4787-804e-a23fef23ba06:4625ac99-30b5-4df6-a6c5-f840dd406e80/1bf8f1d5-d54a-41e0-b203-d94deae18a3c]
primary_tag: c1a376dd-ebd0-4787-804e-a23fef23ba06:d1e7ae78-4202-470c-bf32-eef58f395288/9fa7ee94-dd61-4dcb-bd6f-d6fce4c53cf5
time: 752
author_profile: https://github.com/ksAutotests
author_name: ksAutotests
---
### You will learn
- You will learn this
- and that

autotest tutorial textV805J7

## Prerequisites
- Prerequisute1
- Prerequisute2
- Prerequisute3

[ACCORDION-BEGIN [](fed3492f)]
11775d16-b97f-47da-b8d1-8118aa76281d

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

[ACCORDION-BEGIN [](15bb907b)]
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
06071d29

[OPTION END]

[ACCORDION-END]

[ACCORDION-BEGIN [](c01e4b46)]
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
1eacce6b

[OPTION END]

[OPTION BEGIN [third]]
![image](https://www.sap.com/favicon.ico)
[OPTION END]

[ACCORDION-END]

