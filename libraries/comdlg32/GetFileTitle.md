<link rel="stylesheet" type="text/css" href="../../css/win32api.css">  
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/4.7.0/css/font-awesome.min.css">

## Functionname : GetFileTitle
Group: Common Dialog Box - Library: comdlg32    
***  


#### Retrieves the name of the specified file.
***  


## Code examples:
[Extracting the name and extension parts of a path string](../../samples/sample_118.md)  

## Declaration:
```foxpro  
short GetFileTitle(
  LPCTSTR lpszFile,  // path and file name
  LPTSTR lpszTitle,  // file name buffer
  WORD cbBuf         // length of buffer
);  
```  
***  


## FoxPro declaration:
```foxpro  
DECLARE SHORT GetFileTitle IN Comdlg32;
	STRING   lpszFile,;
	STRING @ lpszTitle,;
	INTEGER  cbBuf  
```  
***  


## Parameters:
```txt  
lpszFile
[in] Pointer to the name and location of a file.

lpszTitle
[out] Pointer to a buffer that receives the name of the file.

cbBuf
[in] Specifies the length, in TCHARs, of the buffer pointed to by the lpszTitle parameter.  
```  
***  


## Return value:
If the function succeeds, the return value is zero. If the file name is invalid, the return value is unknown. 
  
***  


## Comments:
In other words this function extracts the file and extension parts from a legal Win32 path string. Although that does not mean that file should exist.  
  
***  
