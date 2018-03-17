<link rel="stylesheet" type="text/css" href="../../css/win32api.css">  
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/4.7.0/css/font-awesome.min.css">

## Functionname : SetThreadDesktop
Group: Window Station and Desktop - Library: user32    
***  


#### Assigns the specified desktop to the calling thread. All subsequent operations on the desktop use the access rights granted to hDesktop.
***  


## Code examples:
[How to prevent users from accessing the Windows Desktop and from switching to other applications](../../samples/sample_492.md)  

## Declaration:
```foxpro  
BOOL SetThreadDesktop(
	HDESK hDesktop
);
  
```  
***  


## FoxPro declaration:
```foxpro  
DECLARE INTEGER SetThreadDesktop IN user32;
	INTEGER hDesktop  
```  
***  


## Parameters:
```txt  
hDesktop
[in] Handle to the desktop to be assigned to the calling thread. This handle is returned by the CreateDesktop, GetThreadDesktop, OpenDesktop, or OpenInputDesktop function.  
```  
***  


## Return value:
If the function succeeds, the return value is nonzero.  
***  


## Comments:
See also: CreateDesktop, GetThreadDesktop, OpenDesktop, SetProcessWindowStation  
  
***  
