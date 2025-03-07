---
UID: NN:strmif.IMemAllocatorNotifyCallbackTemp
title: IMemAllocatorNotifyCallbackTemp (strmif.h)
description: Enables a filter to receive a callback notification from an allocator whenever a sample is returned to the allocator's free list.
helpviewer_keywords: ["IMemAllocatorNotifyCallbackTemp","IMemAllocatorNotifyCallbackTemp interface [DirectShow]","IMemAllocatorNotifyCallbackTemp interface [DirectShow]","described","IMemAllocatorNotifyCallbackTempInterface","dshow.imemallocatornotifycallbacktemp","strmif/IMemAllocatorNotifyCallbackTemp"]
old-location: dshow\imemallocatornotifycallbacktemp.htm
tech.root: dshow
ms.assetid: 63097b58-8197-4354-8b92-25baaf265df2
ms.date: 12/05/2018
ms.keywords: IMemAllocatorNotifyCallbackTemp, IMemAllocatorNotifyCallbackTemp interface [DirectShow], IMemAllocatorNotifyCallbackTemp interface [DirectShow],described, IMemAllocatorNotifyCallbackTempInterface, dshow.imemallocatornotifycallbacktemp, strmif/IMemAllocatorNotifyCallbackTemp
f1_keywords:
- strmif/IMemAllocatorNotifyCallbackTemp
dev_langs:
- c++
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Strmiids.lib
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Strmiids.lib
- Strmiids.dll
api_name:
- IMemAllocatorNotifyCallbackTemp
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMemAllocatorNotifyCallbackTemp interface


## -description


<p class="CCE_Message">[<b>IMemAllocatorNotifyCallbackTemp</b> is available for use in the operating 

systems specified in the Requirements section. It may be altered or unavailable in 

subsequent versions.]

The <b>IMemAllocatorNotifyCallbackTemp</b> interface enables a filter to receive a callback notification from an allocator whenever a sample is returned to the allocator's free list. To receive callbacks, the filter must implement this interface. For more information, see <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-imemallocatorcallbacktemp">IMemAllocatorCallbackTemp Interface</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMemAllocatorNotifyCallbackTemp</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMemAllocatorNotifyCallbackTemp</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMemAllocatorNotifyCallbackTemp</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-imemallocatornotifycallbacktemp-notifyrelease">NotifyRelease</a>
</td>
<td align="left" width="63%">
Called when a sample returns to the allocator's free list.

</td>
</tr>
</table> 

