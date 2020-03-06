---
title: autotest855L58
description: autotestg83fam_3/6/2020 3:32:25 AM
tags: [topic:139269250608756787992873,products:tech/73554900100700000996,tutorial:experience/advanced]
primary_tag: tutorial:product/sapHana
time: 82
author_profile: https://github.com/ksAutotests
author_name: ksAutotests
---
### You will learn
- You will learn this
- and that

autotest tutorial textTg1F63

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

[ACCORDION-BEGIN [](Unspecified Sql example)]
Sql

```
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

[ACCORDION-BEGIN [](Unspecified Cds example)]
Cds

```
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

[ACCORDION-BEGIN [](Unspecified Css example)]
Css

```
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

[ACCORDION-BEGIN [](Unspecified Cpp example)]
Cpp

```
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

[ACCORDION-BEGIN [](Unspecified R example)]
R

```
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

[ACCORDION-BEGIN [](Unspecified Java example)]
Java

```
package org.intellij.grammar.parser;

import com.intellij.lang.PsiBuilder;
import com.intellij.lang.PsiBuilder.Marker;
import static org.intellij.grammar.psi.BnfTypes.*;
import static org.intellij.grammar.parser.GeneratedParserUtilBase.*;
import com.intellij.psi.tree.IElementType;
import com.intellij.lang.ASTNode;
import com.intellij.psi.tree.TokenSet;
import com.intellij.lang.PsiParser;
import com.intellij.lang.LightPsiParser;

@SuppressWarnings({"SimplifiableIfStatement", "UnusedAssignment"})
public class GrammarParser implements PsiParser, LightPsiParser {

  public ASTNode parse(IElementType t, PsiBuilder b) {
    parseLight(t, b);
    return b.getTreeBuilt();
  }

  public void parseLight(IElementType t, PsiBuilder b) {
    boolean r;
    b = adapt_builder_(t, b, this, EXTENDS_SETS_);
    Marker m = enter_section_(b, 0, _COLLAPSE_, null);
    if (t == BNF_ATTR) {
      r = attr(b, 0);
    }
    else if (t == BNF_ATTR_PATTERN) {
      r = attr_pattern(b, 0);
    }

  // attr_pattern?
  private static boolean attr_1(PsiBuilder b, int l) {
    if (!recursion_guard_(b, l, "attr_1")) return false;
    attr_pattern(b, l + 1);
    return true;
  }

  // ';'?
  private static boolean attr_4(PsiBuilder b, int l) {
    if (!recursion_guard_(b, l, "attr_4")) return false;
    consumeToken(b, BNF_SEMICOLON);
    return true;
  }
...
  };
  final static Parser rule_recover_until_parser_ = new Parser() {
    public boolean parse(PsiBuilder b, int l) {
      return rule_recover_until(b, l + 1);
    }
  };
}
```
[ACCORDION-END]

[ACCORDION-BEGIN [](Unspecified Abap example)]
Abap

```
*/**
* The MIT License (MIT)
* Copyright (c) 2012 René van Mil
* 
* Permission is hereby granted, free of charge, to any person obtaining
* a copy of this software and associated documentation files (the
* SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
*/

*----------------------------------------------------------------------*
*       CLASS CL_CSV_PARSER DEFINITION
*----------------------------------------------------------------------*
*
*----------------------------------------------------------------------*
class cl_csv_parser definition
  public
  inheriting from cl_object
  final
  create public .

  public section.
*"* public components of class CL_CSV_PARSER
*"* do not include other source files here!!!


*----------------------------------------------------------------------*
*       CLASS CL_CSV_PARSER IMPLEMENTATION
*----------------------------------------------------------------------*
*
*----------------------------------------------------------------------*
class cl_csv_parser implementation.


* <SIGNATURE>---------------------------------------------------------------------------------------+
* | Instance Public Method CL_CSV_PARSER->CONSTRUCTOR
* +-------------------------------------------------------------------------------------------------+
* | [--->] DELEGATE                       TYPE REF TO IF_CSV_PARSER_DELEGATE
* | [--->] CSVSTRING                      TYPE        STRING
* | [--->] SEPARATOR                      TYPE        C
* | [--->] SKIP_FIRST_LINE                TYPE        ABAP_BOOL
* +--------------------------------------------------------------------------------------</SIGNATURE>
  method constructor.
    super->constructor( ).
    _delegate = delegate.
    _csvstring = csvstring.
    _separator = separator.
    _skip_first_line = skip_first_line.
  endmethod.                    "constructor


      if _skip_first_line = abap_true and is_first_line = abap_true.
        is_first_line = abap_false.
        continue.
      endif.
      " Parse the line
      data values type standard table of string.
      values = _parse_line( <line> ).
      " Send values to delegate
      _delegate->values_found( values ).
    endloop.
  endmethod.                    "parse


* <SIGNATURE>---------------------------------------------------------------------------------------+
* | Instance Private Method CL_CSV_PARSER->_LINES
* +-------------------------------------------------------------------------------------------------+
* | [<-()] RETURNING                      TYPE        STRINGTAB
* +--------------------------------------------------------------------------------------</SIGNATURE>
  method _lines.
    split _csvstring at cl_abap_char_utilities=>cr_lf into table returning.
  endmethod.                    "_lines


* <SIGNATURE>---------------------------------------------------------------------------------------+
* | Instance Private Method CL_CSV_PARSER->_PARSE_LINE
* +-------------------------------------------------------------------------------------------------+
* | [--->] LINE                           TYPE        STRING
* | [<-()] RETURNING                      TYPE        STRINGTAB
* | [!CX!] CX_CSV_PARSE_ERROR
* +--------------------------------------------------------------------------------------</SIGNATURE>
  method _parse_line.
    data msg type string.

    data csvvalue type string.
    data csvvalues type standard table of string.

    data char type c.
    data pos type i value 0.
    data len type i.
    len = strlen( line ).
    while pos < len.
      char = line+pos(1).
      if char <> _separator.
        if char = _textindicator.
          data text_ended type abap_bool.
          text_ended = abap_false.
          while text_ended = abap_false.
            pos = pos + 1.
            if pos < len.
   
              text_ended = abap_true.
              message e003(csv) into msg.
              raise exception type cx_csv_parse_error
                exporting
                  message = msg.
```
[ACCORDION-END]

[ACCORDION-BEGIN [](Unspecified Swift example)]
Swift

```
let apples = 3
let oranges = 5
let appleSummary = "I have \(apples) apples."
let fruitSummary = "I have \(apples + oranges) pieces of fruit."
class TriangleAndSquare {
    var triangle: EquilateralTriangle {
        willSet {
            square.sideLength = newValue.sideLength
        }
    }
    var square: Square {
        willSet {
            triangle.sideLength = newValue.sideLength
        }
    }
    init(size: Double, name: String) {
        square = Square(sideLength: size, name: name)
        triangle = EquilateralTriangle(sideLength: size, name: name)
    }
}
var triangleAndSquare = TriangleAndSquare(size: 10, name: "another test shape")
triangleAndSquare.square.sideLength
triangleAndSquare.triangle.sideLength
triangleAndSquare.square = Square(sideLength: 50, name: "larger square")
triangleAndSquare.triangle.sideLength
enum ServerResponse {
    case Result(String, String)
    case Error(String)
}

let success = ServerResponse.Result("6:00 am", "8:09 pm")
let failure = ServerResponse.Error("Out of cheese.")

switch success {
    case let .Result(sunrise, sunset):
        let serverResponse = "Sunrise is at \(sunrise) and sunset is at \(sunset)."
    case let .Error(error):
        let serverResponse = "Failure...  \(error)"
}
extension Int: ExampleProtocol {
    var simpleDescription: String {
        return "The number \(self)"
    }
    mutating func adjust() {
        self += 42
    }
 }
7.simpleDescription
```
[ACCORDION-END]

[ACCORDION-BEGIN [](Unspecified Http example)]
Http

```
GET /hello.htm HTTP/1.1
User-Agent: Mozilla/4.0 (compatible; MSIE5.01; Windows NT)
Host: www.tutorialspoint.com
Accept-Language: en-us
Accept-Encoding: gzip, deflate
Connection: Keep-Alive
```
[ACCORDION-END]

[ACCORDION-BEGIN [](Unspecified Xml example)]
Xml

```
<?xml version="1.0" encoding="utf-8"?>
<Project ToolsVersion="12.0" DefaultTargets="Build" xmlns="http://schemas.microsoft.com/developer/msbuild/2003">
  <Import Project="$(MSBuildExtensionsPath)\$(MSBuildToolsVersion)\Microsoft.Common.props" Condition="Exists('$(MSBuildExtensionsPath)\$(MSBuildToolsVersion)\Microsoft.Common.props')" />
  <PropertyGroup>
    <Configuration Condition=" '$(Configuration)' == '' ">Debug</Configuration>
    <Platform Condition=" '$(Platform)' == '' ">AnyCPU</Platform>
    <ProjectGuid>{99D9BF15-2911-4D10-8079-83ABAD688E8B}</ProjectGuid>
    <OutputType>Exe</OutputType>
    <AppDesignerFolder>Properties</AppDesignerFolder>
    <RootNamespace>csproj_sample</RootNamespace>
    <AssemblyName>csproj-sample</AssemblyName>
    <TargetFrameworkVersion>v4.5.1</TargetFrameworkVersion>
    <FileAlignment>512</FileAlignment>
    <AutoGenerateBindingRedirects>true</AutoGenerateBindingRedirects>
...
  <Target Name="AfterBuild">
  </Target>
  -->
</Project>
```
[ACCORDION-END]

[ACCORDION-BEGIN [](Unspecified Html example)]
Html

```
<!DOCTYPE html>
<html>
<head>
<title>Page Title</title>
</head>
<body>

<h1>This is a Heading</h1>
<p>This is a paragraph.</p>

</body>
</html>
```
[ACCORDION-END]

[ACCORDION-BEGIN [](Unspecified Python example)]
Python

```
import re
import sys
import urllib2
import BeautifulSoup

usage = "Run the script: ./geolocate.py IPAddress"

if len(sys.argv)!=2:
    print(usage)
    sys.exit(0)

if len(sys.argv) > 1:
    ipaddr = sys.argv[1]

geody = "http://www.geody.com/geoip.php?ip=" + ipaddr
html_page = urllib2.urlopen(geody).read()
soup = BeautifulSoup.BeautifulSoup(html_page)

# Filter paragraph containing geolocation info.
paragraph = soup('p')[3]

# Remove html tags using regex.
geo_txt = re.sub(r'<.*?>', '', str(paragraph))
print geo_txt[32:].strip()
```
[ACCORDION-END]

[ACCORDION-BEGIN [](Unspecified Json example)]
Json

```
{
     "firstName": "John",
     "lastName" : "Smith",
     "age"      : 25,
     "address"  :
     {
         "streetAddress": "21 2nd Street",
         "city"         : "New York",
         "state"        : "NY",
         "postalCode"   : "10021"
     },
     "phoneNumber":
     [
         {
           "type"  : "home",
           "number": "212 555-1234"
         },
         {
           "type"  : "fax",
           "number": "646 555-4567"
         }
     ]
 }
 {
        "name":"Product",
        "properties":
        {
                "id":
                {
                        "type":"number",
                        "description":"Product identifier",
                        "required":true
                },
                "name":
   
        "id": 1,
        "name": "Foo",
        "price": 123,
        "tags": ["Bar","Eek"],
        "stock": { "warehouse":300, "retail":20 }
}
```
[ACCORDION-END]

[ACCORDION-BEGIN [](Unspecified ShelL example)]
ShelL

```
$ chmod a+x name.sh
$ ./name.sh Hans-Wolfgang Loidl
My first name is Hans-Wolfgang
My surname is Loidl
Total number of arguments is 2
```
[ACCORDION-END]

[ACCORDION-BEGIN [](Unspecified Yaml example)]
Yaml

```
# This is the main configuration file of the Code-Maven web site
appname: "Code::Maven"
layout: "system"
 
# when the charset is set to UTF-8 Dancer will handle for you
# all the magic of encoding and decoding. You should not care
# about unicode within your app when this setting is set (recommended).
charset: "UTF-8"
 
mymaven_yml: "config/mymaven.yml"
 
template: "template_toolkit"
engines:
  template:
    template_toolkit:
      encoding:  'utf8'
      INCLUDE_PATH:
        - 'views'
        - 'config/templates'
      start_tag: '<%'
      end_tag:   '%>'
 
session: "JSON"
```
[ACCORDION-END]

[ACCORDION-BEGIN [](Unspecified Ini example)]
Ini

```
[owner]
name=John Doe
organization=Acme Widgets Inc.

[database]
; use IP address in case network name resolution is not working
server=192.0.2.62     
port=143
file="payroll.dat"
```
[ACCORDION-END]

[ACCORDION-BEGIN [](Unspecified Javascript example)]
Javascript

```
rg) {
  20 line
  quit;
function fancyAlert(arg) { function fancyAlert(arg) {function fancyAlert(arg) {function fancyAlert(arg) {function fancyAlert(arg) {function fancyAlert(arg) {function fancyAlert(arg) { 
  if(arg) {
    $.facebox({div:'#foo'})
  }
}
function fancyAlert(arg) {
  if(arg) {
    $.facebox({div:'#foo'})
  }
}
function fancyAlert(arg) {
  if(arg) {
    $.facebox({div:'#foo'})
  }
}
...
  if(arg) {
    $.facebox({div:'#foo'})
  }
}
```
[ACCORDION-END]

