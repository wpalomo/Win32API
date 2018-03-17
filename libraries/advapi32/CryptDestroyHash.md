<link rel="stylesheet" type="text/css" href="../../css/win32api.css">  
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/4.7.0/css/font-awesome.min.css">

## Functionname : CryptDestroyHash
Group: Cryptography Reference - Library: advapi32    
***  


#### The CryptDestroyHash function destroys the hash object referenced by the hHash parameter. After a hash object has been destroyed, it can no longer be used.
***  


## Code examples:
[CryptoAPI: Collection of Providers class](../../samples/sample_463.md)  
[How to create MD-5 and SHA-1 hash values from a string](../../samples/sample_483.md)  
[A class that encrypts and decrypts files using Cryptography API Functions](../../samples/sample_511.md)  

## Declaration:
```foxpro  
BOOL WINAPI CryptDestroyHash(
  HCRYPTHASH hHash
);  
```  
***  


## FoxPro declaration:
```foxpro  
DECLARE INTEGER CryptDestroyHash IN advapi32;
	INTEGER hHash  
```  
***  


## Parameters:
```txt  
hHash
[in] Handle of the hash object to be destroyed.  
```  
***  


## Return value:
If the function succeeds, the return value is TRUE.  
***  


## Comments:
There should be a one-to-one correspondence between calls to CryptCreateHash and CryptDestroyHash.  
  
***  
