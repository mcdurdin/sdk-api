---
UID: NN:emptyvc.IEmptyVolumeCache2
title: IEmptyVolumeCache2 (emptyvc.h)
description: Extends IEmptyVolumeCache. This interface defines one additional method, InitializeEx, that provides better localization support than IEmptyVolumeCache::Initialize.
helpviewer_keywords: ["IEmptyVolumeCache2","IEmptyVolumeCache2 interface [Legacy Windows Environment Features]","IEmptyVolumeCache2 interface [Legacy Windows Environment Features]","described","_win32_IEmptyVolumeCache2","emptyvc/IEmptyVolumeCache2","lwef.iemptyvolumecache2","shell.iemptyvolumecache2"]
old-location: lwef\iemptyvolumecache2.htm
tech.root: lwef
ms.assetid: a3e941ee-0477-48a8-96bd-c9d74c66ca41
ms.date: 12/05/2018
ms.keywords: IEmptyVolumeCache2, IEmptyVolumeCache2 interface [Legacy Windows Environment Features], IEmptyVolumeCache2 interface [Legacy Windows Environment Features],described, _win32_IEmptyVolumeCache2, emptyvc/IEmptyVolumeCache2, lwef.iemptyvolumecache2, shell.iemptyvolumecache2
f1_keywords:
- emptyvc/IEmptyVolumeCache2
dev_langs:
- c++
req.header: emptyvc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Shell32.dll
api_name:
- IEmptyVolumeCache2
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IEmptyVolumeCache2 interface


## -description


Extends <a href="https://docs.microsoft.com/windows/desktop/api/emptyvc/nn-emptyvc-iemptyvolumecache">IEmptyVolumeCache</a>. This interface defines one additional method, <a href="https://docs.microsoft.com/windows/desktop/api/emptyvc/nf-emptyvc-iemptyvolumecache2-initializeex">InitializeEx</a>, that provides better localization support than <a href="https://docs.microsoft.com/windows/desktop/api/emptyvc/nf-emptyvc-iemptyvolumecache-initialize">IEmptyVolumeCache::Initialize</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEmptyVolumeCache2</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/emptyvc/nn-emptyvc-iemptyvolumecache">IEmptyVolumeCache</a>. <b>IEmptyVolumeCache2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IEmptyVolumeCache2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/emptyvc/nf-emptyvc-iemptyvolumecache2-initializeex">InitializeEx</a>
</td>
<td align="left" width="63%">
Initializes the disk cleanup handler. It provides better support for localization than <a href="https://docs.microsoft.com/windows/desktop/api/emptyvc/nf-emptyvc-iemptyvolumecache-initialize">IEmptyVolumeCache::Initialize</a>.

</td>
</tr>
</table> 


## -remarks



This interface should be exported by disk cleanup handlers running on Windows 2000. Handlers running on Windows 98 must export <a href="https://docs.microsoft.com/windows/desktop/api/emptyvc/nn-emptyvc-iemptyvolumecache">IEmptyVolumeCache</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/emptyvc/nn-emptyvc-iemptyvolumecache">IEmptyVolumeCache</a>



<a href="https://docs.microsoft.com/windows/desktop/api/emptyvc/nn-emptyvc-iemptyvolumecachecallback">IEmptyVolumeCacheCallBack</a>
 

 

