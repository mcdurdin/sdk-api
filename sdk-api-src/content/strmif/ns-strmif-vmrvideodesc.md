---
UID: NS:strmif._VMRVideoDesc
title: VMRVideoDesc (strmif.h)
description: This topic applies to Windows XP Service Pack 1 or later. The VMRVideoDesc structure describes a video stream to be deinterlaced.
helpviewer_keywords: ["FALSE","TRUE","VMRVideoDesc","VMRVideoDesc structure [DirectShow]","VMRVideoDescStructure","dshow.vmrvideodesc","strmif/VMRVideoDesc"]
old-location: dshow\vmrvideodesc.htm
tech.root: dshow
ms.assetid: b02683ec-9bf9-4a69-87fb-d37a98f02e61
ms.date: 12/05/2018
ms.keywords: FALSE, TRUE, VMRVideoDesc, VMRVideoDesc structure [DirectShow], VMRVideoDescStructure, dshow.vmrvideodesc, strmif/VMRVideoDesc
f1_keywords:
- strmif/VMRVideoDesc
dev_langs:
- c++
req.header: strmif.h
req.include-header: Dshow.h
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
- HeaderDef
api_location:
- strmif.h
api_name:
- VMRVideoDesc
targetos: Windows
req.typenames: VMRVideoDesc
req.redist: 
ms.custom: 19H1
---

# VMRVideoDesc structure


## -description



This topic applies to Windows XP Service Pack 1 or later.
          

The <code>VMRVideoDesc</code> structure describes a video stream to be deinterlaced.




## -struct-fields




### -field dwSize

Size of the structure, in bytes.


### -field dwSampleWidth

Width of the video to be deinterlaced, in pixels.


### -field dwSampleHeight

Height of the video to be deinterlaced, in pixels.


### -field SingleFieldPerSample

Specifies one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TRUE"></a><a id="true"></a><dl>
<dt><b><b>TRUE</b></b></dt>
</dl>
</td>
<td width="60%">
Each field is delivered as a separate sample.

</td>
</tr>
<tr>
<td width="40%"><a id="FALSE"></a><a id="false"></a><dl>
<dt><b><b>FALSE</b></b></dt>
</dl>
</td>
<td width="60%">
Pairs of fields are combined into single samples.

</td>
</tr>
</table>
 


### -field dwFourCC

Specifies a FOURCC code. Valid values include NV12, YV12, YUY2, UYVY, IMC1, IMC2, IMC3 and IMC4


### -field InputSampleFreq

A [VMRFrequency](https://docs.microsoft.com/windows/desktop/api/strmif/ns-strmif-vmrfrequency) structure that specifies the input frequency. For NTSC TV, the frequency would be expressed as 30,000:1001.


### -field OutputFrameFreq

A 
              [VMRFrequency](https://docs.microsoft.com/windows/desktop/api/strmif/ns-strmif-vmrfrequency) structure that specifies the output frequency. For NTSC TV, the frequency would be expressed as 60,000:1001.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/directshow-structures">DirectShow Structures</a>
 

 

