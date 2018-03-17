<link rel="stylesheet" type="text/css" href="../../css/win32api.css">  
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/4.7.0/css/font-awesome.min.css">

## Functionname : GdipNewInstalledFontCollection
Group: GDI+ Font - Library: gdiplus    
***  


#### Represents the fonts installed on the system
***  


## Code examples:
[Custom GDI+ class](../../samples/sample_450.md)  

## Declaration:
```foxpro  
GpStatus WINGDIPAPI GdipNewInstalledFontCollection(
	GpFontCollection** fontCollection
)
  
```  
***  


## FoxPro declaration:
```foxpro  
DECLARE INTEGER GdipNewInstalledFontCollection IN gdiplus;
	INTEGER @ fontCollection  
```  
***  


## Parameters:
```txt  
fontCollection
[out] Handle to the FontCollection object.  
```  
***  


## Return value:
Returns 0 on success.  
***  
