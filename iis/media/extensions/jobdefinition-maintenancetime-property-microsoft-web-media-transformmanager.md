﻿---
title: JobDefinition.MaintenanceTime Property  (Microsoft.Web.Media.TransformManager)
TOCTitle: MaintenanceTime Property
ms:assetid: P:Microsoft.Web.Media.TransformManager.JobDefinition.MaintenanceTime
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/microsoft.web.media.transformmanager.jobdefinition.maintenancetime(v=VS.90)
ms:contentKeyID: 35520630
ms.date: 06/14/2012
mtps_version: v=VS.90
f1_keywords:
- Microsoft.Web.Media.TransformManager.JobDefinition.get_MaintenanceTime
- Microsoft.Web.Media.TransformManager.JobDefinition.MaintenanceTime
- Microsoft.Web.Media.TransformManager.JobDefinition.set_MaintenanceTime
dev_langs:
- CSharp
- JScript
- VB
- FSharp
- c++
api_location:
- Microsoft.Web.Media.TransformManager.Common.dll
api_name:
- Microsoft.Web.Media.TransformManager.JobDefinition.get_MaintenanceTime
- Microsoft.Web.Media.TransformManager.JobDefinition.MaintenanceTime
- Microsoft.Web.Media.TransformManager.JobDefinition.set_MaintenanceTime
api_type:
- Managed
topic_type:
- apiref
- kbSyntax
product_family_name: VS
ROBOTS: INDEX,FOLLOW
---

# MaintenanceTime Property

Gets or sets a fixed time during the day to run maintenance.

**Namespace:**  [Microsoft.Web.Media.TransformManager](microsoft-web-media-transformmanager-namespace.md)  
**Assembly:**  Microsoft.Web.Media.TransformManager.Common (in Microsoft.Web.Media.TransformManager.Common.dll)

## Syntax

``` vb
'Declaration
<DataMemberAttribute> _
PublicPropertyMaintenanceTimeAsDateTimeGetSet
'Usage
DiminstanceAsJobDefinitionDimvalueAsDateTimevalue = instance.MaintenanceTime

instance.MaintenanceTime = value
```

``` csharp
[DataMemberAttribute]
publicDateTimeMaintenanceTime { get; set; }
```

``` c++
[DataMemberAttribute]
public:
propertyDateTimeMaintenanceTime {
    DateTimeget ();
    voidset (DateTimevalue);
}
```

``` fsharp
[<DataMemberAttribute>]
memberMaintenanceTime : DateTimewithget, set
```

``` jscript
function getMaintenanceTime () : DateTimefunction setMaintenanceTime (value : DateTime)
```

#### Property Value

Type: [System. . :: . .DateTime](https://msdn.microsoft.com/en-us/library/03ybds8y\(v=vs.90\))  
A fixed time during the day to run maintenance.  

## See Also

#### Reference

[JobDefinition Class](jobdefinition-class-microsoft-web-media-transformmanager.md)

[Microsoft.Web.Media.TransformManager Namespace](microsoft-web-media-transformmanager-namespace.md)
