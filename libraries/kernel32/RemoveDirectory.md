<link rel="stylesheet" type="text/css" href="../../css/win32api.css">  
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/4.7.0/css/font-awesome.min.css">

## Functionname : RemoveDirectory
Group: File Management - Library: kernel32    
***  


#### The RemoveDirectory function deletes an existing empty directory. To recursively delete files and subdirectories in a directory, use the SHFileOperation function.
***  


## Declaration:
```foxpro  
BOOL RemoveDirectory(
  LPCTSTR lpPathName   // directory name
);  
```  
***  


## FoxPro declaration:
```foxpro  
DECLARE INTEGER RemoveDirectory IN kernel32;
	STRING lpPathName  
```  
***  


## Parameters:
```txt  
lpPathName
[in] Pointer to a null-terminated string that specifies the path of the directory to be removed. The path must specify an empty directory, and the calling process must have delete access to the directory  
```  
***  


## Return value:
If the function succeeds, the return value is nonzero  
***  


## Comments:
To recursively delete the files in a directory, use the SHFileOperation function.  
  
See also: RemoveDirectoryTransacted   
  
***  
