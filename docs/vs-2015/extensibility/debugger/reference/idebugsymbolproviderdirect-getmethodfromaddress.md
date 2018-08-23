---
title: "IDebugSymbolProviderDirect::GetMethodFromAddress | Microsoft Docs"
ms.custom: ""
ms.date: "2018-06-30"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "vs-ide-sdk"
ms.tgt_pltfrm: ""
ms.topic: "article"
helpviewer_keywords: 
  - "IDebugSymbolProviderDirect::GetMethodFromAddress"
  - "GetMethodFromAddress"
ms.assetid: 33ffd197-1221-41bc-a9f6-f133ebdcb783
caps.latest.revision: 9
ms.author: "gregvanl"
manager: "ghogen"
---
# IDebugSymbolProviderDirect::GetMethodFromAddress
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

The latest version of this topic can be found at [IDebugSymbolProviderDirect::GetMethodFromAddress](https://docs.microsoft.com/visualstudio/extensibility/debugger/reference/idebugsymbolproviderdirect-getmethodfromaddress).  
  
Retrieves information about the method at the specified debug address.  
  
## Syntax  
  
```cpp#  
HRESULT GetMethodFromAddress(  
   IDebugAddress* pAddress,  
   GUID*          pGuid,  
   DWORD*         pAppID,  
   _mdToken*      pTokenClass,  
   _mdToken*      pTokenMethod,  
   DWORD*         pdwOffset,  
   DWORD*         pdwVersion  
);  
```  
  
```csharp  
int GetMethodFromAddress(  
   IDebugAddress pAddress,  
   out Guid      pGuid,  
   out uint      pAppID,  
   out uint      pTokenClass,  
   out uint      pTokenMethod,  
   out uint      pdwOffset,  
   out uint      pdwVersion  
);  
```  
  
#### Parameters  
 `pAddress`  
 [in] Debug address that is represented by the [IDebugAddress](../../../extensibility/debugger/reference/idebugaddress.md) interface.  
  
 `pGuid`  
 [out] Unique identifier of the module.  
  
 `pAppID`  
 [out] Identifier of the application domain.  
  
 `pTokenClass`  
 [out] Token that represents the containing class.  
  
 `pTokenMethod`  
 [out] Token that represents the module.  
  
 `pdwOffset`  
 [out] An offset in bytes from the start of the `pAddress` parameter.  
  
 `pdwVersion`  
 [out] Version number of the method.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns an error code.  
  
## See Also  
 [IDebugSymbolProviderDirect](../../../extensibility/debugger/reference/idebugsymbolproviderdirect.md)
