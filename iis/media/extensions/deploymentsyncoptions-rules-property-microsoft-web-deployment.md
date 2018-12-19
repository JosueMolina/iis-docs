﻿---
title: DeploymentSyncOptions.Rules Property  (Microsoft.Web.Deployment)
TOCTitle: Rules Property
ms:assetid: P:Microsoft.Web.Deployment.DeploymentSyncOptions.Rules
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/microsoft.web.deployment.deploymentsyncoptions.rules(v=VS.90)
ms:contentKeyID: 20208873
ms.date: 05/02/2012
mtps_version: v=VS.90
f1_keywords:
- Microsoft.Web.Deployment.DeploymentSyncOptions.Rules
- Microsoft.Web.Deployment.DeploymentSyncOptions.get_Rules
dev_langs:
- CSharp
- JScript
- VB
- c++
api_location:
- Microsoft.Web.Deployment.dll
api_name:
- Microsoft.Web.Deployment.DeploymentSyncOptions.get_Rules
- Microsoft.Web.Deployment.DeploymentSyncOptions.Rules
api_type:
- Managed
topic_type:
- apiref
- kbSyntax
product_family_name: VS
ROBOTS: INDEX,FOLLOW
---

# Rules Property

Gets a collection of [DeploymentRule](deploymentrule-class-microsoft-web-deployment.md) objects associated with the current object instance.

**Namespace:**  [Microsoft.Web.Deployment](microsoft-web-deployment-namespace.md)  
**Assembly:**  Microsoft.Web.Deployment (in Microsoft.Web.Deployment.dll)

## Syntax

``` vb
'Declaration
PublicReadOnlyPropertyRulesAsDeploymentRuleCollection
'Usage
DiminstanceAsDeploymentSyncOptionsDimvalueAsDeploymentRuleCollectionvalue = instance.Rules
```

``` csharp
publicDeploymentRuleCollectionRules { get; }
```

``` c++
public:
propertyDeploymentRuleCollection^ Rules {
    DeploymentRuleCollection^ get ();
}
```

``` jscript
function getRules () : DeploymentRuleCollection
```

#### Property Value

Type: [Microsoft.Web.Deployment. . :: . .DeploymentRuleCollection](deploymentrulecollection-class-microsoft-web-deployment.md)  
A [DeploymentRuleCollection](deploymentrulecollection-class-microsoft-web-deployment.md) that contains [DeploymentRule](deploymentrule-class-microsoft-web-deployment.md) objects associated with the current object instance.  

## Examples

The following example implements the class [DeploymentSyncOptions](deploymentsyncoptions-class-microsoft-web-deployment.md)by calling the static method [GetAvailableRules](deploymentsyncoptions-getavailablerules-method-microsoft-web-deployment.md) to get currently available rules that will apply to the sync operation. A [DeploymentSyncOptions](deploymentsyncoptions-class-microsoft-web-deployment.md) instance then modifies properties: [WhatIf](deploymentsyncoptions-whatif-property-microsoft-web-deployment.md) and [UseChecksum](deploymentsyncoptions-usechecksum-property-microsoft-web-deployment.md).

**Note**   The [WhatIf](deploymentsyncoptions-whatif-property-microsoft-web-deployment.md) property allows for the possibility of performing a trial sync in order to determine the possibility of a sync operation and to provide a measurement of the changes that might occur in used in conjunction with an instance of [DeploymentChangeSummary](deploymentchangesummary-class-microsoft-web-deployment.md).

using System;

using Microsoft.Web.Deployment;

namespace MSDeploy.Web.Deployment

{

class Program

{

static void Main(string\[\] args)

{

// List currently available rules

foreach(DeploymentRule rule in

DeploymentSyncOptions.GetAvailableRules())

{

Console.WriteLine("Description: " + rule.Description);

Console.WriteLine("ExampleOrDetail: " + rule.ExampleOrDetail);

Console.WriteLine("FriendlyName: " + rule.FriendlyName);

Console.WriteLine("Name: " + rule.Name);

Console.WriteLine("Handler: " +

rule.RuleHandler.ToString());

Console.WriteLine();

}

DeploymentSyncOptions syncOptions = new DeploymentSyncOptions();

syncOptions.WhatIf = true; // report expected results of

// syncing without performing a sync operation

syncOptions.UseChecksum = true; // compare files through

// checksum to determine if they should be synced

DeploymentBaseOptions sourceBaseOptions =

new DeploymentBaseOptions();

DeploymentBaseOptions destinationBaseOptions =

new DeploymentBaseOptions();

DeploymentObject deploymentObject =

DeploymentManager.CreateObject(

DeploymentWellKnownProvider.AppHostConfig,

"Default Web Site", sourceBaseOptions);

DeploymentChangeSummary changes =

deploymentObject.SyncTo(

DeploymentWellKnownProvider.AppHostConfig,

"Default Web Site2", destinationBaseOptions,

syncOptions);

Console.WriteLine("Added: " +

changes.ObjectsAdded.ToString());

Console.WriteLine("Updated: " +

changes.ObjectsUpdated.ToString());

Console.WriteLine("Deleted: " +

changes.ObjectsDeleted.ToString());

Console.WriteLine("Errors: " +

changes.Errors.ToString());

}

}

}

## Permissions

  - Full trust for the immediate caller. This member cannot be used by partially trusted code. For more information, see [Using Libraries from Partially Trusted Code](https://msdn.microsoft.com/en-us/library/8skskf63\(v=vs.90\)).

## See Also

#### Reference

[DeploymentSyncOptions Class](deploymentsyncoptions-class-microsoft-web-deployment.md)

[Microsoft.Web.Deployment Namespace](microsoft-web-deployment-namespace.md)
