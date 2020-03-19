---
title: autotest1Jhq73
description: autotest1MvmqX_3/19/2020 6:23:22 PM
tags: [topic:139269250608756787992873,products:tech/73554900100700000996,tutorial:experience/advanced]
primary_tag: tutorial:product/sapHana
time: 298
author_profile: https://github.com/ksAutotests
author_name: ksAutotests
---
### You will learn
- You will learn this
- and that

autotest tutorial textY82W1q

## Prerequisites
- Prerequisute1
- Prerequisute2
- Prerequisute3

[ACCORDION-BEGIN [](First step)]
[DONE]
[ACCORDION-END]

[ACCORDION-BEGIN [](Second step)]
[DONE]
[ACCORDION-END]

[ACCORDION-BEGIN [](Third step)]
[DONE]
[ACCORDION-END]

[ACCORDION-BEGIN [](Nested 'Sql' language)]
1. First item
2. Second item



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
[ACCORDION-END]

[ACCORDION-BEGIN [](Nested 'Cds' language)]
* First item
* Second item



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
[ACCORDION-END]

[ACCORDION-BEGIN [](Nested 'Css' language)]
>### Warning 
> 



```Css
<!DOCTYPE html>
<html>
<head>
<style>
p {
    border-style: solid;
}

p.none {border-left-style: none;}
p.dotted {border-left-style: dotted;}
p.dashed {border-left-style: dashed;}
p.solid {border-left-style: solid;}
p.double {border-left-style: double;}
p.groove {border-left-style: groove;}
p.ridge {border-left-style: ridge;}
p.inset {border-left-style: inset;}
p.outset {border-left-style: outset;}
</style>
</head>
<body>

<p class="none">No left border.</p>
<p class="dotted">A dotted left border.</p>
<p class="dashed">A dashed left border.</p>
<p class="solid">A solid left border.</p>
<p class="double">A double left border.</p>
<p class="groove">A groove left border.</p>
<p class="ridge">A ridge left border.</p>
<p class="inset">An inset left border.</p>
<p class="outset">An outset left border.</p>

</body>
</html>
```
[ACCORDION-END]

[ACCORDION-BEGIN [](Nested 'Cpp' language)]
1. First item
2. Second item



```Cpp
#include<iostream>

using namespace std;

int main()

{

int var1, var2, swap;

 cout<<"Enter value for first integer:  ";

 cin>>var1;

 cout<<"Enter value for second integer:  ";

 cin>>var2;

// Construct the format name of the private queue. The returned   
  // computer GUID is translated into a string and then combined   
  // with the queue number.  
  UCHAR *pszUuid = 0;                     // Computer GUID string  
  CHAR szFormatNameBuffer[256];           // Format name buffer  
  WCHAR wszFormatNameBuffer[256];         // Wide-character format name buffer  
  
  if (UuidToString(&guidMachineId, &pszUuid) != RPC_S_OK)  
  {  
     fprintf(stderr, "An error occurred in UuidToString.\n");  
     return E_FAIL;  
  }  
  else  
  {  
```
[ACCORDION-END]

[ACCORDION-BEGIN [](Nested 'R' language)]
* First item
* Second item



```R
w = rnorm(500,0,1)  # 500 N(0,1) variates
v = filter(w, sides=2, rep(1/3,3))  # moving average
par(mfrow=c(2,1))
plot.ts(w, main="white noise")
plot.ts(v, ylim=c(-3,3), main="moving average")

# now try this (not in text):  
dev.new()  # open a new graphic device
ts.plot(w, v, lty=2:1, col=1:2, lwd=1:2)
```
[ACCORDION-END]

