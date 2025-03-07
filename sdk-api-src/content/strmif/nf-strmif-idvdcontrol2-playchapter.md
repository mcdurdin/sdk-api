---
UID: NF:strmif.IDvdControl2.PlayChapter
title: IDvdControl2::PlayChapter (strmif.h)
description: The PlayChapter method starts playback from the specified chapter in the current title.
helpviewer_keywords: ["IDvdControl2 interface [DirectShow]","PlayChapter method","IDvdControl2.PlayChapter","IDvdControl2::PlayChapter","IDvdControl2PlayChapter","PlayChapter","PlayChapter method [DirectShow]","PlayChapter method [DirectShow]","IDvdControl2 interface","dshow.idvdcontrol2_playchapter","strmif/IDvdControl2::PlayChapter"]
old-location: dshow\idvdcontrol2_playchapter.htm
tech.root: dshow
ms.assetid: b624aa7e-ff88-417c-8536-4ac38e8ae1ca
ms.date: 12/05/2018
ms.keywords: IDvdControl2 interface [DirectShow],PlayChapter method, IDvdControl2.PlayChapter, IDvdControl2::PlayChapter, IDvdControl2PlayChapter, PlayChapter, PlayChapter method [DirectShow], PlayChapter method [DirectShow],IDvdControl2 interface, dshow.idvdcontrol2_playchapter, strmif/IDvdControl2::PlayChapter
f1_keywords:
- strmif/IDvdControl2.PlayChapter
dev_langs:
- c++
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
- IDvdControl2.PlayChapter
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDvdControl2::PlayChapter


## -description



The <code>PlayChapter</code> method starts playback from the specified chapter in the current title.




## -parameters




### -param ulChapter [in]

Value that specifies the chapter in the current title where the DVD Navigator will start playback; this value must be from 1 through 999.


### -param dwFlags [in]

Bitwise <b>OR</b> of one or more flags from the <a href="https://docs.microsoft.com/windows/desktop/api/strmif/ne-strmif-dvd_cmd_flags">DVD_CMD_FLAGS</a> enumeration, specifying how to synchronize the command.


### -param ppCmd [out]

Receives a pointer to an <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-idvdcmd">IDvdCmd</a> object that can be used to synchronize DVD commands. The caller must release the interface. This parameter can be <b>NULL</b>. For more information, see <a href="https://docs.microsoft.com/windows/desktop/DirectShow/synchronizing-dvd-commands">Synchronizing DVD Commands</a>.


## -returns



Returns one of the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_DVD_OPERATION_INHIBITED</b></dt>
</dl>
</td>
<td width="60%">
UOP control prohibits the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid argument.

</td>
</tr>
</table>
 




## -remarks



The DVD Navigator begins playback at the specified chapter and continues to the subsequent chapters. Use <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-idvdcontrol2-playchaptersautostop">IDvdControl2::PlayChaptersAutoStop</a> to play the current chapter only.

The following table shows the Annex J command name to which this method name corresponds, and the domains in which this method is valid.

This method is demonstrated in the DVDSample application in <b>CDvdCore::PlayChapter</b>.

<table>
<tr>
<td>Annex J Command Name
            </td>
<td>Valid Domains
            </td>
</tr>
<tr>
<td>PTT_Search</td>
<td>DVD_DOMAIN_Title</td>
</tr>
</table>
 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/dvd-applications">DVD Applications</a>



<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-idvdcontrol2">IDvdControl2 Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/DirectShow/synchronizing-dvd-commands">Synchronizing DVD Commands</a>
 

 

