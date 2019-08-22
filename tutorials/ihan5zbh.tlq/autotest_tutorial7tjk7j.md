---
title: autotestj1JO32
description: autotest02gd1u_8/22/2019 10:16:34 AM
tags: [topic:139269250608756787992873,products:tech/73554900100700000996,tutorial:experience/advanced]
primary_tag: tutorial:product/sapHana
time: 135
author_profile: https://github.com/ksAutotests
author_name: ksAutotests
---
### You will learn
- You will learn this
- and that

autotest tutorial text85wbMA

## Prerequisites
- Prerequisute1
- Prerequisute2
- Prerequisute3

[ACCORDION-BEGIN [](679617c1-b0ec-419a-a693-ec25b91b9e53)]
b5be949a-968b-4835-aa2b-0befbddd4d5c

[ACCORDION-END]

[ACCORDION-BEGIN [](b75d3190-7b61-4be0-8629-bb6ae3d54cb6)]
eafe2bbd-347f-4fce-8381-7f9cb9840caa

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

[ACCORDION-BEGIN [](d47ff606-e02e-4c5a-aaac-9531f2925c89)]
6df4efbd-2eae-4e61-9eaf-6e31add15646

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

