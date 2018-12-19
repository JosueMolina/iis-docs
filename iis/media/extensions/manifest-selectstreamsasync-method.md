﻿---
title: Manifest.SelectStreamsAsync Method
TOCTitle: SelectStreamsAsync Method
ms:assetid: 839f4238-95ce-466f-b41a-4d8db65542ff
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/JJ822765(v=VS.90)
ms:contentKeyID: 50079520
ms.date: 11/19/2012
mtps_version: v=VS.90
dev_langs:
- csharp
- c++
- jscript
---

# Manifest.SelectStreamsAsync Method

**Applies to:** Windows Store apps only

Select the streams in the current manifest.

## Syntax

``` csharp
public IAsyncOperation<IVectorView<IStreamChangedResult>> SelectStreamsAsync(
IVectorView<IManifestStream> pStreams
)
```

``` c++
public:
virtual IAsyncOperation<IVectorView<IStreamChangedResult^>^>^ SelectStreamsAsync(
[InAttribute] IVectorView<IManifestStream^>^ pStreams
) sealed
```

``` jscript
public final function SelectStreamsAsync(
pStreams : IVectorView<IManifestStream>
) : IAsyncOperation<IVectorView<IStreamChangedResult>>
```

## Return Value

If the method succeeds, it returns S\_OK. Otherwise, it returns an HRESULT error code.

## Requirements

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Minimum supported client</strong></p></td>
<td><p>Windows 8</p></td>
</tr>
<tr class="even">
<td><p><strong>Minimum supported server</strong></p></td>
<td><p>Not Supported</p></td>
</tr>
<tr class="odd">
<td><p><strong>Metadata</strong></p></td>
<td><p>Microsoft.Media.AdaptiveStreaming.winmd</p></td>
</tr>
</tbody>
</table>
