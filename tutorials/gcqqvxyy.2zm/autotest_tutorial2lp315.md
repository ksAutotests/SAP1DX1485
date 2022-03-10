---
title: autotestZ5boDh
description: autotestlME78k_3/10/2022 5:58:07 AM
tags: [82352407468693968798155:325f896d-bad5-49ee-a4e6-518589778cd8/139269250608756787992873,197f4ec4-6c14-5b5e-9fb3-058e21403d41:tech/73554900100700000996,c1a376dd-ebd0-4787-804e-a23fef23ba06:4625ac99-30b5-4df6-a6c5-f840dd406e80/1bf8f1d5-d54a-41e0-b203-d94deae18a3c]
primary_tag: 197f4ec4-6c14-5b5e-9fb3-058e21403d41:tech/73554900100700000996/67838200100800006287
time: 886
author_profile: https://github.com/ksAutotests
author_name: ksAutotests
---
### You will learn
- You will learn this
- and that

autotest tutorial textDZhFsI

## Prerequisites
- Prerequisute1
- Prerequisute2
- Prerequisute3

[ACCORDION-BEGIN [](3225f7ab)]
cd43432d-88bd-40d5-97ee-c632162a566f

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

[ACCORDION-BEGIN [](c80784a4)]
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
abc437e5

[OPTION END]

[ACCORDION-END]

[ACCORDION-BEGIN [](62589c50)]
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
237d11e0

[OPTION END]

[OPTION BEGIN [third]]
![image](https://www.sap.com/favicon.ico)
[OPTION END]

[ACCORDION-END]

