<link rel="stylesheet" type="text/css" href="../../css/win32api.css">  
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/4.7.0/css/font-awesome.min.css">

## Functionname : AVIStreamGetFrameClose
Group: Windows Multimedia - Library: avifil32    
***  


#### The AVIStreamGetFrameClose function releases resources used to decompress video frames.
***  


## Code examples:
[How to play AVI file on the _screen](../../samples/sample_430.md)  
[How to extract frames from AVI files](../../samples/sample_484.md)  

## Declaration:
```foxpro  
STDAPI AVIStreamGetFrameClose(
  PGETFRAME pget
);  
```  
***  


## FoxPro declaration:
```foxpro  
DECLARE INTEGER AVIStreamGetFrameClose IN avifil32;
	INTEGER pget  
```  
***  


## Parameters:
```txt  
pget
Handle returned from the AVIStreamGetFrameOpen function.
  
```  
***  


## Return value:
Returns zero if successful or an error otherwise.  
***  
