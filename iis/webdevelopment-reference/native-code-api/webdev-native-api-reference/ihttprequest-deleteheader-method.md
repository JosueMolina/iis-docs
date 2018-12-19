---
title: "IHttpRequest::DeleteHeader Method | Microsoft Docs"
ms.custom: ""
ms.date: "10/07/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 922cd9ec-3c4d-81f8-581e-e7d81683c716
caps.latest.revision: 27
author: "shirhatti"
manager: "wpickett"
---
# IHttpRequest::DeleteHeader Method
Deletes an HTTP header from the request.  
  
## Syntax  
  
```cpp  
virtual HRESULT DeleteHeader(  
   IN PCSTR pszHeaderName  
) = 0;  
  
virtual HRESULT DeleteHeader(  
   IN HTTP_HEADER_ID ulHeaderIndex  
) = 0;  
```  
  
#### Parameters  
 `pszHeaderName`  
 [IN] A pointer to a string that contains the name of the header to delete.  
  
 `ulHeaderIndex`  
 [IN] An `HTTP_HEADER_ID` value that specifies the ID of an HTTP header to delete.  
  
## Return Value  
 An `HRESULT`. Possible values include, but are not limited to, those in the following table.  
  
|Value|Description|  
|-----------|-----------------|  
|S_OK|Indicates that the operation was successful.|  
  
## Remarks  
 The `DeleteHeader` method deletes a specified HTTP header from the current request. There are two overloaded versions of the `DeleteHeader` method. One specifies the header by using a string that is contained in the `pszHeaderName` parameter. The other overload uses an unsigned long integer that is contained in the `ulHeaderIndex` parameter.  
  
 The header name specified by the `pszHeaderName` parameter can be a custom header or a header defined in Request for Comments (RFC) 1945, "Hypertext Transfer Protocol -- HTTP/1.0," or RFC 2616, "Hypertext Transfer Protocol -- HTTP/1.1."  
  
> [!NOTE]
>  The `pszHeaderName` parameter cannot be set to `null`.  
  
 The `ulHeaderIndex` parameter specifies the ID of an HTTP header that is listed in the `HTTP_HEADER_ID` enumeration, which contains several common HTTP headers.  
  
> [!NOTE]
>  The `HTTP_HEADER_ID` enumeration is defined in the Http.h header file.  
  
## Example  
 The following code example illustrates how to use both versions of the `DeleteHeader` method to create an HTTP module that removes the `User-Agent` and `Accept-Language` HTTP headers from the request.  
  
<!-- TODO: review snippet reference  [!CODE [IHttpRequestDeleteHeader#1](IHttpRequestDeleteHeader#1)]  -->  
  
 Your module must export the [RegisterModule](../../../webdevelopment-reference\native-code-api\webdev-native-api-reference/pfn-registermodule-function.md) function. You can export this function by creating a module definition (.def) file for your project, or you can compile the module by using the `/EXPORT:RegisterModule` switch. For more information, see [Walkthrough: Creating a Request-Level HTTP Module By Using Native Code](../../../webdevelopment-reference\native-code-development-overview\native-code-dev-overview/walkthrough-creating-a-request-level-http-module-by-using-native-code.md).  
  
 You can optionally compile the code by using the `__stdcall (/Gz)` calling convention instead of explicitly declaring the calling convention for each function.  
  
## Requirements  
  
|Type|Description|  
|----------|-----------------|  
|Client|-   [!INCLUDE[iis70](../../../wmi-provider/includes/iis70-md.md)] on [!INCLUDE[winvista](../../../wmi-provider/includes/winvista-md.md)]<br />-   [!INCLUDE[iis75](../../../wmi-provider/includes/iis75-md.md)] on [!INCLUDE[win7](../../../wmi-provider/includes/win7-md.md)]<br />-   [!INCLUDE[iis80](../../../wmi-provider/includes/iis80-md.md)] on [!INCLUDE[win8](../../../wmi-provider/includes/win8-md.md)]<br />-   [!INCLUDE[iis100](../../../wmi-provider/includes/iis100-md.md)] on [!INCLUDE[win10](../../../wmi-provider/includes/win10-md.md)]|  
|Server|-   [!INCLUDE[iis70](../../../wmi-provider/includes/iis70-md.md)] on [!INCLUDE[winsrv2008](../../../wmi-provider/includes/winsrv2008-md.md)]<br />-   [!INCLUDE[iis75](../../../wmi-provider/includes/iis75-md.md)] on [!INCLUDE[winsrv2008r2](../../../wmi-provider/includes/winsrv2008r2-md.md)]<br />-   [!INCLUDE[iis80](../../../wmi-provider/includes/iis80-md.md)] on [!INCLUDE[winsrv2012](../../../wmi-provider/includes/winsrv2012-md.md)]<br />-   [!INCLUDE[iis85](../../../wmi-provider/includes/iis85-md.md)] on [!INCLUDE[winsrv2012r2](../../../wmi-provider/includes/winsrv2012r2-md.md)]<br />-   [!INCLUDE[iis100](../../../wmi-provider/includes/iis100-md.md)] on [!INCLUDE[winsrv2016](../../../wmi-provider/includes/winsrv2016-md.md)]|  
|Product|-   [!INCLUDE[iis70](../../../wmi-provider/includes/iis70-md.md)], [!INCLUDE[iis75](../../../wmi-provider/includes/iis75-md.md)], [!INCLUDE[iis80](../../../wmi-provider/includes/iis80-md.md)], [!INCLUDE[iis85](../../../wmi-provider/includes/iis85-md.md)], [!INCLUDE[iis100](../../../wmi-provider/includes/iis100-md.md)]<br />-   [!INCLUDE[iisexp75](../../../webdevelopment-reference\native-code-api\webdev-native-api-reference/includes/iisexp75-md.md)], [!INCLUDE[iisexp80](../../../webdevelopment-reference\native-code-api\webdev-native-api-reference/includes/iisexp80-md.md)], [!INCLUDE[iisexp100](../../../webdevelopment-reference\native-code-api\webdev-native-api-reference/includes/iisexp100-md.md)]|  
|Header|Httpserv.h|  
  
## See Also  
 [IHttpRequest Interface](../../../webdevelopment-reference\native-code-api\webdev-native-api-reference/ihttprequest-interface.md)   
 [IHttpRequest::GetHeader Method](../../../webdevelopment-reference\native-code-api\webdev-native-api-reference/ihttprequest-getheader-method.md)   
 [IHttpRequest::SetHeader Method](../../../webdevelopment-reference\native-code-api\webdev-native-api-reference/ihttprequest-setheader-method.md)