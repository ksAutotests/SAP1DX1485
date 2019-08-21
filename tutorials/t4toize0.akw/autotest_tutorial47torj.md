---
title: autotestt688R2
description: autotestx1R8sq_8/21/2019 4:45:05 PM
tags: [topic:139269250608756787992873,products:tech/73554900100700000996,tutorial:experience/advanced]
primary_tag: tutorial:product/sapHana
time: 208
author_profile: https://github.com/ksAutotests
author_name: ksAutotests
---
### You will learn
- You will learn this
- and that

autotest tutorial textZZ5wG8

## Prerequisites
- Prerequisute1
- Prerequisute2
- Prerequisute3

[ACCORDION-BEGIN [](eb43cdee-5a37-44af-bd5d-4c1042e6952f)]
28c24bd9-8c02-4a67-97ff-1e22c629494d

[ACCORDION-END]

[ACCORDION-BEGIN [](bba75a36-c2e0-4d74-bfd5-d7d9b960a8db)]
ea2e4232-a383-45c8-8667-7e3da83f95db

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

[ACCORDION-BEGIN [](774b5bff-b410-42ac-929b-35d29dcc5d9b)]
e31f8f26-1b45-4f62-8368-43614efdabb9

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

