<link rel="stylesheet" type="text/css" href="../css/win32api.css">  
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/4.7.0/css/font-awesome.min.css">

# Retrieving the command line for the VFP session

## Before you begin:
See also:

* [How to: Use Command-Line Options When Starting Visual FoxPro](sample_000.md)  

  
***  


## Code:
```foxpro  
DO declare

LOCAL nAddress, cBuffer, nBufsize
nAddress = GetCommandLine()  && returns an address in memory
nBufsize = GlobalSize(nAddress)

* allocating and filling a buffer
IF nBufsize <> 0
	cBuffer = Repli(Chr(0), nBufsize)
	= CopyMemory(@cBuffer, nAddress, nBufsize)
ELSE
* a possibility in Win98/Me
	cBuffer = Repli(Chr(0), 512)
	= CopyMemory(@cBuffer, nAddress, 512)
	cBuffer = SUBSTR(cBuffer, 1, AT(Chr(0)+Chr(0),cBuffer)+1)
ENDIF

cBuffer = STRTRAN(cBuffer, CHR(0), "")
? "Command line: [" + cBuffer + "]"

PROCEDURE declare
	DECLARE INTEGER GetCommandLine IN kernel32

	DECLARE INTEGER GlobalSize IN kernel32;
		INTEGER hMem

	DECLARE RtlMoveMemory IN kernel32;
	As CopyMemory;
		STRING @Destination, INTEGER Source,;
		INTEGER nLength  
```  
***  


## Listed functions:
[GetCommandLine](../libraries/kernel32/GetCommandLine.md)  
[GlobalSize](../libraries/kernel32/GlobalSize.md)  