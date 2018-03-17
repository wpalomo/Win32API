<link rel="stylesheet" type="text/css" href="../../css/win32api.css">  
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/4.7.0/css/font-awesome.min.css">

## Functionname : GetMouseMovePointsEx
Group: Mouse Input - Library: user32    
***  


#### Retrieves a history of up to 64 previous coordinates of the mouse or pen.
***  


## Code examples:
[GDI+: Implementing image scrolling with inertia](../../samples/sample_595.md)  

## Declaration:
```foxpro  
int WINAPI GetMouseMovePointsEx(
  _In_   UINT cbSize,
  _In_   LPMOUSEMOVEPOINT lppt,
  _Out_  LPMOUSEMOVEPOINT lpptBuf,
  _In_   int nBufPoints,
  _In_   DWORD resolution
);  
```  
***  


## FoxPro declaration:
```foxpro  
DECLARE INTEGER GetMouseMovePointsEx IN user32;
	INTEGER cbSize,;
	STRING @lppt,;
	STRING @lpptBuf,;
	INTEGER nBufPoints,;
	INTEGER resolution  
```  
***  


## Parameters:
```txt  
cbSize [in]
The size, in bytes, of the MOUSEMOVEPOINT structure.

lppt [in]
A pointer to a MOUSEMOVEPOINT structure containing valid mouse coordinates (in screen coordinates). It may also contain a time stamp.

lpptBuf [out]
A pointer to a buffer that will receive the points. It should be at least cbSize* nBufPoints in size.

nBufPoints [in]
The number of points to be retrieved (up to 64).

resolution [in]
The resolution desired: GMMP_USE_DISPLAY_POINTS (1), GMMP_USE_HIGH_RESOLUTION_POINTS (2)  
```  
***  


## Return value:
If the function succeeds, the return value is the number of points in the buffer.  
***  


## Comments:
See also: GetCursorPos, GetTickCount   
  
***  
