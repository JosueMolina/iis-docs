---
title: "GetVersionObject | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 98e42cf9-bcd4-4e1e-a01d-f8e44052e93d
caps.latest.revision: 10
manager: "wpickett"
---
# GetVersionObject
Returns the installed IIS version based on version and product type.  
  
## Syntax  
  
```cpp  
    HRESULT  
    GetVersionObject(  
        [in, string] BSTR  bstrVersion,  
        [in] IIS_PRODUCT_TYPE dwProductType,  
        [out, retval] IIISVersion ** ppElement  
    );  
  
```  
  
#### Parameters  
  
-   [in, string] BSTR  `bstrVersion`  
  
     The version of the product to get, in *major.minor* format. This can be an empty string (""); in that case, the method returns the highest version of the product specified in the `dwProductType` parameter.  
  
-   [in] IIS_PRODUCT_TYPE `dwProductType`  
  
     The product type of the version object, specified as a value in the [IIS_PRODUCT_TYPE](../../extenions\express-api-ref/iis-product-type.md) enumeration.  
  
-   [out, retval] IIISVersion `** ppElement`  
  
     If the specified product type and version is found on the computer, returns the appropriate [IIISVersion](../../extenions\express-api-ref/iiisversion.md) object.  
  
## Return Value  
 `HRESULT`  
  
## See Also  
 [GetAllVersionObjects](../../extenions\express-api-ref/getallversionobjects.md)