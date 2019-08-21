---
title: autotestD1r32e
description: autotests7T4r5_8/21/2019 3:50:44 PM
tags: [topic:139269250608756787992873,products:tech/73554900100700000996,tutorial:experience/advanced]
primary_tag: tutorial:product/sapHana
time: 458
author_profile: https://github.com/ksAutotests
author_name: ksAutotests
---
### You will learn
- You will learn this
- and that

autotest tutorial textkp4Bb4

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

[ACCORDION-BEGIN [](36f82970-d0b1-497f-82dd-b2af34aa6298)]
0501c035-3f93-47dd-8600-d780ac91f255

[ACCORDION-END]

[ACCORDION-BEGIN [](7f0dd472-c09a-4c03-b3a2-3829d22e6c88)]
8c157614-4632-4616-b4f4-30de811558bd

[OPTION BEGIN [conditional1]]
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

[ACCORDION-END]

[ACCORDION-BEGIN [](0681ac7d-8125-44a5-8d11-70a0d53affd7)]
d25eb07b-2e1b-4577-9772-3bce5bf1f7de

[OPTION BEGIN [conditional2]]
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
[OPTION END]

[OPTION BEGIN [conditional1]]
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

[ACCORDION-END]

