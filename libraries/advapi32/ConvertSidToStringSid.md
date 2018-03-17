<link rel="stylesheet" type="text/css" href="../../css/win32api.css">  
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/4.7.0/css/font-awesome.min.css">

## Functionname : ConvertSidToStringSid
Group: Security - Library: advapi32    
***  


#### Converts a security identifier (SID) to a string format suitable for display, storage, or transmission.
***  


## Code examples:
[Retrieving local computer and user names](../../samples/sample_041.md)  

## Declaration:
```foxpro  
BOOL ConvertSidToStringSid(
  PSID Sid,
  LPTSTR* StringSid
);  
```  
***  


## FoxPro declaration:
```foxpro  
DECLARE INTEGER ConvertSidToStringSid IN advapi32;
	INTEGER Sid,;
	INTEGER @StringSid  
```  
***  


## Parameters:
```txt  
Sid
[in] Pointer to the SID structure to convert.

StringSid
[out] Pointer to a variable that receives a pointer to a null-terminated SID string. To free the returned buffer, call the LocalFree function.  
```  
***  


## Return value:
If the function succeeds, the return value is nonzero.  
***  


## Comments:
Examples of what this function returns:  
S-1-800  
S-1-5-21-606747154-839522115-1708537768-1004  
  
***  
