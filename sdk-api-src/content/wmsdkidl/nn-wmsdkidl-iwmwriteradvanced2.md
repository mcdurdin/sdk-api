---
UID: NN:wmsdkidl.IWMWriterAdvanced2
title: IWMWriterAdvanced2 (wmsdkidl.h)
description: The IWMWriterAdvanced2 interface provides the ability to set and retrieve named settings for an input.IWMWriterAdvanced2 exists for every instance of the writer object. To obtain a pointer to this interface, call QueryInterface on the writer object.
helpviewer_keywords: ["IWMWriterAdvanced2","IWMWriterAdvanced2 interface [windows Media Format]","IWMWriterAdvanced2 interface [windows Media Format]","described","IWMWriterAdvanced2Interface","wmformat.iwmwriteradvanced2","wmsdkidl/IWMWriterAdvanced2"]
old-location: wmformat\iwmwriteradvanced2.htm
tech.root: wmformat
ms.assetid: 94790b67-690c-4a0f-9b82-801bfcec9eb0
ms.date: 12/05/2018
ms.keywords: IWMWriterAdvanced2, IWMWriterAdvanced2 interface [windows Media Format], IWMWriterAdvanced2 interface [windows Media Format],described, IWMWriterAdvanced2Interface, wmformat.iwmwriteradvanced2, wmsdkidl/IWMWriterAdvanced2
f1_keywords:
- wmsdkidl/IWMWriterAdvanced2
dev_langs:
- c++
req.header: wmsdkidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- wmsdkidl.h
api_name:
- IWMWriterAdvanced2
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMWriterAdvanced2 interface


## -description



The <b>IWMWriterAdvanced2</b> interface provides the ability to set and retrieve named settings for an input.

<b>IWMWriterAdvanced2</b> exists for every instance of the writer object. To obtain a pointer to this interface, call <b>QueryInterface</b> on the writer object.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMWriterAdvanced2</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced">IWMWriterAdvanced</a>. <b>IWMWriterAdvanced2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMWriterAdvanced2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-getinputsetting">GetInputSetting</a>
</td>
<td align="left" width="63%">
Retrieves a setting for a particular input by name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting">SetInputSetting</a>
</td>
<td align="left" width="63%">
Specifies a named setting for a particular input.

</td>
</tr>
</table> 

For information about which interfaces can be obtained by using the QueryInterface method of this interface, see <a href="https://docs.microsoft.com/windows/desktop/wmformat/writer-object">Writer Object</a>.



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriter">IWMWriter Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced">IWMWriterAdvanced Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced3">IWMWriterAdvanced3 Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/wmformat/interfaces">Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/wmformat/writer-object">Writer Object</a>



<a href="https://docs.microsoft.com/windows/desktop/wmformat/writing-asf-files">Writing ASF Files</a>
 

 

