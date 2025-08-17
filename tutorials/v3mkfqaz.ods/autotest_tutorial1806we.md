---
title: autotest28xXd6
description: autotest81HwXV_8/17/2025 2:53:24 PM
tags: [82352407468693968798155:325f896d-bad5-49ee-a4e6-518589778cd8/139269250608756787992873,197f4ec4-6c14-5b5e-9fb3-058e21403d41:tech/73554900100700000996,c1a376dd-ebd0-4787-804e-a23fef23ba06:4625ac99-30b5-4df6-a6c5-f840dd406e80/1bf8f1d5-d54a-41e0-b203-d94deae18a3c]
primary_tag: 197f4ec4-6c14-5b5e-9fb3-058e21403d41:tech/73554900100700000996/67838200100800006287
time: 166
author_profile: https://github.com/ksAutotests
author_name: ksAutotests
---
### You will learn
- You will learn this
- and that

autotest tutorial text7g13N8

## Prerequisites
- Prerequisute1
- Prerequisute2
- Prerequisute3

[ACCORDION-BEGIN [](6e0a556f)]
fa9a9481-2450-49a5-bad1-e8641da2a915

[OPTION BEGIN [first]]
```Abap
*/**
* The MIT License (MIT)
* Copyright (c) 2012 Ren� van Mil
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
[OPTION END]

[ACCORDION-END]

[ACCORDION-BEGIN [](7eb2cd41)]
[OPTION BEGIN [first]]
```C++
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
[OPTION END]

[OPTION BEGIN [second]]
568f99c6

[OPTION END]

[ACCORDION-END]

[ACCORDION-BEGIN [](7635b880)]
[OPTION BEGIN [first]]
```C++
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
[OPTION END]

[OPTION BEGIN [second]]
f43198ae

[OPTION END]

[OPTION BEGIN [third]]
![image](https://www.sap.com/favicon.ico)
[OPTION END]

[ACCORDION-END]

