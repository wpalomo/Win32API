<link rel="stylesheet" type="text/css" href="../css/win32api.css">  
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/4.7.0/css/font-awesome.min.css">

# Using the SetErrorMode for determining if a floppy drive is ready

## Before you begin:
A try to read a floppy-drive that is not ready produces both -- the Windows, and VFP -- error messages under VFP3+WinNT4. In this situation the following code does make a sense. Otherwise under VFP6+WinMe there is no system error message. So ON ERROR redirection is quite enough.  
  
***  


## Code:
```foxpro  
#DEFINE SEM_FAILCRITICALERRORS 1
#DEFINE SEM_NOALIGNMENTFAULTEXCEPT 4
#DEFINE SEM_NOGPFAULTERRORBOX 2
#DEFINE SEM_NOOPENFILEERRORBOX 0x8000

DECLARE INTEGER SetErrorMode IN kernel32 INTEGER uMode

LOCAL lvOldOnError, lnVfpError, lnOldErrorMode

* saving the old ErroMode value, and at the same moment
* suppressing a possible system message of no disk in drive
lnOldMode = SetErrorMode (SEM_FAILCRITICALERRORS)

* saving the old ON ERROR state
lvOldOnError = ON("ERROR")
lnVfpError = .F.
ON ERROR lnVfpError = .T.

SET CONS OFF
DIR a:
SET CONS ON

* restoring saved properties
ON ERROR &lvOldOnError
= SetErrorMode (lnOldMode)

RETURN  Not lnVfpError  
```  
***  


## Listed functions:
[SetErrorMode](../libraries/kernel32/SetErrorMode.md)  