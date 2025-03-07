---
UID: NF:ole2.OleDraw
title: OleDraw function (ole2.h)
description: Enables drawing objects more easily. You can use it instead of calling IViewObject::Draw directly.
helpviewer_keywords: ["OleDraw","OleDraw function [COM]","_ole_OleDraw","com.oledraw","ole/OleDraw"]
old-location: com\oledraw.htm
tech.root: com
ms.assetid: c45c6746-59ea-43bb-9f2b-2182d7a3fc7a
ms.date: 12/05/2018
ms.keywords: OleDraw, OleDraw function [COM], _ole_OleDraw, com.oledraw, ole/OleDraw
f1_keywords:
- ole2/OleDraw
dev_langs:
- c++
req.header: ole2.h
req.include-header: Ole2.h
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
req.lib: Ole32.lib
req.dll: Ole32.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- Ole32.dll
- ext-ms-win-com-ole32-l1-1-3.dll
- Ext-MS-Win-Com-Ole32-L1-1-4.dll
api_name:
- OleDraw
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# OleDraw function


## -description


Enables drawing objects more easily. You can use it instead of calling <a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nf-oleidl-iviewobject-draw">IViewObject::Draw</a> directly.


## -parameters




#### - pUnknown [in]

Pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface on the view object that is to be drawn.


#### - dwAspect [in]

How the object is to be represented. Representations include content, an icon, a thumbnail, or a printed document. Possible values are taken from the <a href="https://docs.microsoft.com/windows/desktop/api/wtypes/ne-wtypes-dvaspect">DVASPECT</a> enumeration.


#### - hdcDraw [in]

Device context on which to draw. Cannot be a metafile device context.


#### - lprcBounds [in]

Pointer to a <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure specifying the rectangle in which the object should be drawn. This parameter is converted to a <a href="https://docs.microsoft.com/previous-versions/dd162907(v=vs.85)">RECTL</a> structure and passed to <a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nf-oleidl-iviewobject-draw">IViewObject::Draw</a>.


## -returns



This function returns S_OK on success. Other possible values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OLE_E_BLANK</b></dt>
</dl>
</td>
<td width="60%">
No data to draw from.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ABORT</b></dt>
</dl>
</td>
<td width="60%">
The draw operation was aborted.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VIEW_E_DRAW</b></dt>
</dl>
</td>
<td width="60%">
No data to draw from.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OLE_E_INVALIDRECT</b></dt>
</dl>
</td>
<td width="60%">
The rectangle is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG </b></dt>
</dl>
</td>
<td width="60%">
One or more parameters are invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory for the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DV_E_NOIVIEWOBJECT</b></dt>
</dl>
</td>
<td width="60%">
The object doesn't support the <a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nn-oleidl-iviewobject">IViewObject</a> interface.

</td>
</tr>
</table>
 




## -remarks



The OleDraw helper function calls the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> method for the object specified (pUnk), asking for an <a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nn-oleidl-iviewobject">IViewObject</a> interface on that object. Then, <b>OleDraw</b> converts the <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure to a <a href="https://docs.microsoft.com/previous-versions/dd162907(v=vs.85)">RECTL</a> structure, and calls <a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nf-oleidl-iviewobject-draw">IViewObject::Draw</a> as follows:

<pre class="syntax" xml:space="preserve"><code>lpViewObj-&gt;Draw(dwAspect,-1,0,0,0,hdcDraw,&amp;rectl,0,0,0);</code></pre>
Do not use this function to draw into a metafile because it does not specify the parameter required for drawing into metafiles.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nf-oleidl-iviewobject-draw">IViewObject::Draw</a>
 

 

