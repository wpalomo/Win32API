<link rel="stylesheet" type="text/css" href="../../css/win32api.css">  
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/4.7.0/css/font-awesome.min.css">

## Functionname : OemToChar
Group: String - Library: user32    
***  


#### Translates a string from the OEM-defined character set into either an ANSI or a wide-character string.

***  


## Code examples:
[Converting strings between ANSI and OEM](../../samples/sample_099.md)  

## Declaration:
```foxpro  
BOOL OemToChar(
  LPCSTR lpszSrc,  // string to translate
  LPTSTR lpszDst   // translated string
);  
```  
***  


## FoxPro declaration:
```foxpro  
DECLARE SHORT OemToChar IN user32;
	STRING lpszSrc,;
	STRING @ lpszDst  
```  
***  


## Parameters:
```txt  
lpszSrc
[in] Pointer to a null-terminated string of characters from the OEM-defined character set.

lpszDst
[out] Pointer to the buffer for the translated string.  
```  
***  


## Return value:
The return value is always nonzero except when you pass the same address to lpszSrc and lpszDst in the wide-character version of the function. In this case the function returns zero and GetLastError returns ERROR_INVALID_ADDRESS.  
***  
