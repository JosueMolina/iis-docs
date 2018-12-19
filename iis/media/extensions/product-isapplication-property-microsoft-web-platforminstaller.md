﻿---
title: Product.IsApplication Property  (Microsoft.Web.PlatformInstaller)
TOCTitle: IsApplication Property
ms:assetid: P:Microsoft.Web.PlatformInstaller.Product.IsApplication
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/microsoft.web.platforminstaller.product.isapplication(v=VS.90)
ms:contentKeyID: 22049630
ms.date: 05/02/2012
mtps_version: v=VS.90
f1_keywords:
- Microsoft.Web.PlatformInstaller.Product.IsApplication
- Microsoft.Web.PlatformInstaller.Product.get_IsApplication
- Microsoft.Web.PlatformInstaller.Product.set_IsApplication
dev_langs:
- CSharp
- JScript
- VB
- c++
api_location:
- Microsoft.Web.PlatformInstaller.dll
api_name:
- Microsoft.Web.PlatformInstaller.Product.get_IsApplication
- Microsoft.Web.PlatformInstaller.Product.IsApplication
- Microsoft.Web.PlatformInstaller.Product.set_IsApplication
api_type:
- Managed
topic_type:
- apiref
- kbSyntax
product_family_name: VS
ROBOTS: INDEX,FOLLOW
---

# IsApplication Property

Gets or sets a value that indicates whether the product is an application.

**Namespace:**  [Microsoft.Web.PlatformInstaller](microsoft-web-platforminstaller-namespace.md)  
**Assembly:**  Microsoft.Web.PlatformInstaller (in Microsoft.Web.PlatformInstaller.dll)

## Syntax

``` vb
'Declaration
PublicPropertyIsApplicationAsBooleanGetFriendSet
'Usage
DiminstanceAsProductDimvalueAsBooleanvalue = instance.IsApplication
```

``` csharp
publicboolIsApplication { get; internalset; }
```

``` c++
public:
propertyboolIsApplication {
    boolget ();
    internal: voidset (boolvalue);
}
```

``` jscript
function getIsApplication () : booleaninternalfunction setIsApplication (value : boolean)
```

#### Property Value

Type: Boolean  
true if the product is an application, otherwise false.  

## Permissions

  - Full trust for the immediate caller. This member cannot be used by partially trusted code. For more information, see <https://msdn.microsoft.com/en-us/library/8skskf63(v=vs.90)>.

## See Also

#### Reference

[Product Class](product-class-microsoft-web-platforminstaller.md)

[Product Members](product-members-microsoft-web-platforminstaller.md)

[Microsoft.Web.PlatformInstaller Namespace](microsoft-web-platforminstaller-namespace.md)
