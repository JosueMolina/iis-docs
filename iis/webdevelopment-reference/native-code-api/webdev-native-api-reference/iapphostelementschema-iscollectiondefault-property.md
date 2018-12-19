---
title: "IAppHostElementSchema::IsCollectionDefault Property | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: ecc6b08c-2abe-49e8-a2d2-2327e6942644
caps.latest.revision: 7
author: "shirhatti"
manager: "wpickett"
---
# IAppHostElementSchema::IsCollectionDefault Property
Gets a corresponding [IAppHostElement Interface](../../../webdevelopment-reference\native-code-api\webdev-native-api-reference/iapphostelement-interface.md) object.  
  
## Syntax  
  
```cpp  
[propget] HRESULT IsCollectionDefault(  
   [out,  
   retval] VARIANT_BOOL * pfIsCollectionDefault  
);  
```  
  
#### Parameters  
 `pfIsCollectionDefault`  
 Contains a Boolean value that indicates whether the corresponding [IAppHostElement Interface](../../../webdevelopment-reference\native-code-api\webdev-native-api-reference/iapphostelement-interface.md) object is a default for other [IAppHostElement Interface](../../../webdevelopment-reference\native-code-api\webdev-native-api-reference/iapphostelement-interface.md) objects.  
  
## Return Value  
 An `HRESULT`. Possible values include, but are not limited to, those in the following table.  
  
|Value|Description|  
|-----------|-----------------|  
|S_OK|Indicates that the operation was successful.|  
  
## Requirements  
  
|Type|Description|  
|----------|-----------------|  
|Client|-   [!INCLUDE[iis70](../../../wmi-provider/includes/iis70-md.md)] on [!INCLUDE[winvista](../../../wmi-provider/includes/winvista-md.md)]<br />-   [!INCLUDE[iis75](../../../wmi-provider/includes/iis75-md.md)] on [!INCLUDE[win7](../../../wmi-provider/includes/win7-md.md)]<br />-   [!INCLUDE[iis80](../../../wmi-provider/includes/iis80-md.md)] on [!INCLUDE[win8](../../../wmi-provider/includes/win8-md.md)]<br />-   [!INCLUDE[iis100](../../../wmi-provider/includes/iis100-md.md)] on [!INCLUDE[win10](../../../wmi-provider/includes/win10-md.md)]|  
|Server|-   [!INCLUDE[iis70](../../../wmi-provider/includes/iis70-md.md)] on [!INCLUDE[winsrv2008](../../../wmi-provider/includes/winsrv2008-md.md)]<br />-   [!INCLUDE[iis75](../../../wmi-provider/includes/iis75-md.md)] on [!INCLUDE[winsrv2008r2](../../../wmi-provider/includes/winsrv2008r2-md.md)]<br />-   [!INCLUDE[iis80](../../../wmi-provider/includes/iis80-md.md)] on [!INCLUDE[winsrv2012](../../../wmi-provider/includes/winsrv2012-md.md)]<br />-   [!INCLUDE[iis85](../../../wmi-provider/includes/iis85-md.md)] on [!INCLUDE[winsrv2012r2](../../../wmi-provider/includes/winsrv2012r2-md.md)]<br />-   [!INCLUDE[iis100](../../../wmi-provider/includes/iis100-md.md)] on [!INCLUDE[winsrv2016](../../../wmi-provider/includes/winsrv2016-md.md)]|  
|Product|-   [!INCLUDE[iis70](../../../wmi-provider/includes/iis70-md.md)], [!INCLUDE[iis75](../../../wmi-provider/includes/iis75-md.md)], [!INCLUDE[iis80](../../../wmi-provider/includes/iis80-md.md)], [!INCLUDE[iis85](../../../wmi-provider/includes/iis85-md.md)], [!INCLUDE[iis100](../../../wmi-provider/includes/iis100-md.md)]<br />-   [!INCLUDE[iisexp75](../../../webdevelopment-reference\native-code-api\webdev-native-api-reference/includes/iisexp75-md.md)], [!INCLUDE[iisexp80](../../../webdevelopment-reference\native-code-api\webdev-native-api-reference/includes/iisexp80-md.md)], [!INCLUDE[iisexp100](../../../webdevelopment-reference\native-code-api\webdev-native-api-reference/includes/iisexp100-md.md)]|  
|Header|Ahadmin.h|  
  
## See Also  
 [IAppHostElement Interface](../../../webdevelopment-reference\native-code-api\webdev-native-api-reference/iapphostelement-interface.md)   
 [IAppHostElementSchema Interface](../../../webdevelopment-reference\native-code-api\webdev-native-api-reference/iapphostelementschema-interface.md)   
 [IAppHostElementSchemaCollection Interface](../../../webdevelopment-reference\native-code-api\webdev-native-api-reference/iapphostelementschemacollection-interface.md)