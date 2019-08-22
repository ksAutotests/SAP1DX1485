---
title: autotestnM7E2Y
description: autotestZcGLg2_8/22/2019 10:27:23 AM
tags: [topic:139269250608756787992873,products:tech/73554900100700000996,tutorial:experience/advanced]
primary_tag: tutorial:product/sapHana
time: 559
author_profile: https://github.com/ksAutotests
author_name: ksAutotests
---
### You will learn
- You will learn this
- and that

autotest tutorial text70vO7d

## Prerequisites
- Prerequisute1
- Prerequisute2
- Prerequisute3

[ACCORDION-BEGIN [](17874d39-1472-4265-bbcd-25a33c4635e7)]
08052f78-97b9-478b-8117-13ad77a33097

[ACCORDION-END]

[ACCORDION-BEGIN [](ba127620-1311-49d3-94c8-443afea54884)]
c3b7b505-40dd-46ad-b438-2ed3881079cb

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

[ACCORDION-BEGIN [](e66b9df4-d9e7-437f-a0db-92de0658e77f)]
5ec2b9de-77be-49d2-83eb-f86da5c2f087

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

