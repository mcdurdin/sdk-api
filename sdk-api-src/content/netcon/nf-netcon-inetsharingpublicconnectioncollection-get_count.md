---
UID: NF:netcon.INetSharingPublicConnectionCollection.get_Count
title: INetSharingPublicConnectionCollection::get_Count (netcon.h)
description: The get_Count method retrieves the number of items in the public connections collection.
helpviewer_keywords: ["INetSharingPublicConnectionCollection interface [ICS/ICF]","get_Count method","INetSharingPublicConnectionCollection.get_Count","INetSharingPublicConnectionCollection::get_Count","_ics_inetsharingpublicconnectioncollection_get_count","get_Count","get_Count method [ICS/ICF]","get_Count method [ICS/ICF]","INetSharingPublicConnectionCollection interface","ics.inetsharingpublicconnectioncollection_get_count","netcon/INetSharingPublicConnectionCollection::get_Count"]
old-location: ics\inetsharingpublicconnectioncollection_get_count.htm
tech.root: ics
ms.assetid: 7d90ce6c-4ac7-4188-9d25-9144e112a8df
ms.date: 12/05/2018
ms.keywords: INetSharingPublicConnectionCollection interface [ICS/ICF],get_Count method, INetSharingPublicConnectionCollection.get_Count, INetSharingPublicConnectionCollection::get_Count, _ics_inetsharingpublicconnectioncollection_get_count, get_Count, get_Count method [ICS/ICF], get_Count method [ICS/ICF],INetSharingPublicConnectionCollection interface, ics.inetsharingpublicconnectioncollection_get_count, netcon/INetSharingPublicConnectionCollection::get_Count
f1_keywords:
- netcon/INetSharingPublicConnectionCollection.get_Count
dev_langs:
- c++
req.header: netcon.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: None supported
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
req.dll: Hnetcfg.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Hnetcfg.dll
api_name:
- INetSharingPublicConnectionCollection.get_Count
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# INetSharingPublicConnectionCollection::get_Count


## -description


<p class="CCE_Message">[Internet Connection Firewall may be altered or unavailable in subsequent versions. Instead, use the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/ics/windows-firewall-start-page">Windows Firewall API</a>.]

The <b>get_Count</b> method retrieves the number of items in the public connections collection.


## -parameters




### -param pVal [out]

Pointer to a <b>long</b> variable that receives the number of items in the public connections collection.


## -returns



If the method succeeds the return value is <b>S_OK</b>.

If the method fails, the return value is one of the following error codes.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ABORT</b></dt>
</dl>
</td>
<td width="60%">
The operation was aborted.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
An unspecified error occurred.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One of the parameters is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOINTERFACE</b></dt>
</dl>
</td>
<td width="60%">
A specified interface is not supported.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
A specified method is not implemented.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
The method was unable to allocate required memory.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
A pointer passed as a parameter is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
The method failed for unknown reasons.

</td>
</tr>
</table>
 




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netcon/nn-netcon-inetsharingpublicconnectioncollection">INetSharingPublicConnectionCollection</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/ics/internet-connection-sharing-and-internet-connection-firewall-interfaces">Internet Connection Sharing and Internet Connection Firewall Interfaces</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/ics/internet-connection-sharing-and-internet-connection-firewall-reference">Internet Connection Sharing and Internet Connection Firewall Reference</a>
 

 

