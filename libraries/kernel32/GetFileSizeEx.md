<link rel="stylesheet" type="text/css" href="../../css/win32api.css">  
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/4.7.0/css/font-awesome.min.css">

## Functionname : GetFileSizeEx
Group: File System - Library: kernel32    
***  


#### The GetFileSizeEx function retrieves the size of the specified file.
***  


## Code examples:
[Using File Mapping for enumerating files opened by Visual FoxPro](../../samples/sample_473.md)  

## Declaration:
```foxpro  
BOOL GetFileSizeEx(
  HANDLE hFile,
  PLARGE_INTEGER lpFileSize
);  
```  
***  


## FoxPro declaration:
```foxpro  
DECLARE INTEGER GetFileSizeEx IN kernel32;
	INTEGER  hFile,;
	STRING @ lpFileSize  
```  
***  


## Parameters:
```txt  
hFile
[in] Handle to the file whose size is to be returned.

lpFileSize
[out] Pointer to a LARGE_INTEGER structure that receives the file size.  
```  
***  


## Return value:
If the function succeeds, the return value is nonzero.  
***  


## Comments:
Client: Requires Windows XP or Windows 2000 Professional.  
Server: Requires Windows Server 2003 or Windows 2000 Server.  
  
The LARGE_INTEGER structure is used to represent a 64-bit signed integer value.  
  
***  
