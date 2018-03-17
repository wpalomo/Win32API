<link rel="stylesheet" type="text/css" href="../../css/win32api.css">  
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/4.7.0/css/font-awesome.min.css">

## Functionname : GetFileVersionInfo
Group: Version Information - Library: version    
***  


#### Retrieves version information for the specified file.
***  


## Code examples:
[How to retrieve version information for the specified file](../../samples/sample_480.md)  

## Declaration:
```foxpro  
BOOL GetFileVersionInfo(
	LPTSTR lptstrFilename,
	DWORD dwHandle,
	DWORD dwLen,
	LPVOID lpData
);  
```  
***  


## FoxPro declaration:
```foxpro  
DECLARE INTEGER GetFileVersionInfo IN version.dll;
	STRING   lptstrFilename,;
	INTEGER  dwHandle,;
	INTEGER  dwLen,;
	STRING @ lpData
  
```  
***  


## Parameters:
```txt  
lptstrFilename
[in] Pointer to a null-terminated string that specifies the name of the file of interest.

dwHandle
This parameter is ignored.

dwLen
[in] Specifies the size, in bytes, of the buffer pointed to by the lpData parameter.

lpData
[out] Pointer to a buffer that receives the file-version information.  
```  
***  


## Return value:
If the function succeeds, the return value is nonzero.  
***  


## Comments:
Call the GetFileVersionInfoSize function first to determine the size, in bytes, of a file"s version information. The <Em>dwLen</Em> member should be equal to or greater than that value.   
  
***  
