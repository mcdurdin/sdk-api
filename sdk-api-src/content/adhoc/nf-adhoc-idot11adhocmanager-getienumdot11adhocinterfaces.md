---
UID: NF:adhoc.IDot11AdHocManager.GetIEnumDot11AdHocInterfaces
title: IDot11AdHocManager::GetIEnumDot11AdHocInterfaces (adhoc.h)
description: Returns the set of wireless network interface cards (NICs) available on the machine.
helpviewer_keywords: ["GetIEnumDot11AdHocInterfaces","GetIEnumDot11AdHocInterfaces method [NativeWIFI]","GetIEnumDot11AdHocInterfaces method [NativeWIFI]","IDot11AdHocManager interface","IDot11AdHocManager interface [NativeWIFI]","GetIEnumDot11AdHocInterfaces method","IDot11AdHocManager.GetIEnumDot11AdHocInterfaces","IDot11AdHocManager::GetIEnumDot11AdHocInterfaces","adhoc/IDot11AdHocManager::GetIEnumDot11AdHocInterfaces","nwifi.idot11adhocmanager_getienumdot11adhocinterfaces"]
old-location: nwifi\idot11adhocmanager_getienumdot11adhocinterfaces.htm
tech.root: nwifi
ms.assetid: 2e705533-3657-4997-ae84-e18defbbc02a
ms.date: 12/05/2018
ms.keywords: GetIEnumDot11AdHocInterfaces, GetIEnumDot11AdHocInterfaces method [NativeWIFI], GetIEnumDot11AdHocInterfaces method [NativeWIFI],IDot11AdHocManager interface, IDot11AdHocManager interface [NativeWIFI],GetIEnumDot11AdHocInterfaces method, IDot11AdHocManager.GetIEnumDot11AdHocInterfaces, IDot11AdHocManager::GetIEnumDot11AdHocInterfaces, adhoc/IDot11AdHocManager::GetIEnumDot11AdHocInterfaces, nwifi.idot11adhocmanager_getienumdot11adhocinterfaces
f1_keywords:
- adhoc/IDot11AdHocManager.GetIEnumDot11AdHocInterfaces
dev_langs:
- c++
req.header: adhoc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Adhoc.idl
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
- adhoc.h
api_name:
- IDot11AdHocManager.GetIEnumDot11AdHocInterfaces
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDot11AdHocManager::GetIEnumDot11AdHocInterfaces


## -description


Returns the set of wireless network interface cards (NICs) available on the machine.


## -parameters




### -param ppEnum [out]

A pointer to an <a href="https://docs.microsoft.com/windows/desktop/api/adhoc/nn-adhoc-ienumdot11adhocinterfaces">IEnumDot11AdHocInterfaces</a> interface that contains the list of NICs.


## -returns



Possible return values include, but are not limited to, the following.

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
The method completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The method failed.

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
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
The method could not allocate the memory required to perform this operation.

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
</table>
 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/adhoc/nn-adhoc-idot11adhocmanager">IDot11AdHocManager</a>
 

 

