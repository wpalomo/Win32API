<link rel="stylesheet" type="text/css" href="../../css/win32api.css">  
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/4.7.0/css/font-awesome.min.css">

## Functionname : GdipSetSmoothingMode
Group: GDI+ Graphics - Library: gdiplus    
***  


#### Sets the rendering quality of the Graphics object.
***  


## Code examples:
[Custom GDI+ class](../../samples/sample_450.md)  

## Declaration:
```foxpro  
GpStatus WINGDIPAPI GdipSetSmoothingMode(
	GpGraphics *graphics,
	SmoothingMode smoothingMode)  
```  
***  


## FoxPro declaration:
```foxpro  
DECLARE INTEGER GdipSetSmoothingMode IN gdiplus;
	INTEGER graphics,;
	INTEGER smoothingMode  
```  
***  


## Parameters:
```txt  
graphics
[in] Handle of a Graphics object.

smoothingMode
[in] Element of the SmoothingMode enumeration.  
```  
***  


## Return value:
Returns Ok (0) if succeeded.  
***  


## Comments:
See also: GdipGetSmoothingMode   
  
<a href="http://msdn.microsoft.com/en-us/library/windows/desktop/ms534173(v=vs.85).aspx">SmoothingMode</a> enumeration.  
  
***  
