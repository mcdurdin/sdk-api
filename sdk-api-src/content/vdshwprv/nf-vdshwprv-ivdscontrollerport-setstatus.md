---
UID: NF:vdshwprv.IVdsControllerPort.SetStatus
title: IVdsControllerPort::SetStatus (vdshwprv.h)
description: Sets the status of a controller port to the specified value.
helpviewer_keywords: ["IVdsControllerPort interface [VDS]","SetStatus method","IVdsControllerPort.SetStatus","IVdsControllerPort::SetStatus","SetStatus","SetStatus method [VDS]","SetStatus method [VDS]","IVdsControllerPort interface","base.ivdscontrollerport_setstatus","vds/IVdsControllerPort::SetStatus","vdshwprv/IVdsControllerPort::SetStatus"]
old-location: base\ivdscontrollerport_setstatus.htm
tech.root: base
ms.assetid: 1338e1e7-80c8-409d-aa54-575618fd9797
ms.date: 12/05/2018
ms.keywords: IVdsControllerPort interface [VDS],SetStatus method, IVdsControllerPort.SetStatus, IVdsControllerPort::SetStatus, SetStatus, SetStatus method [VDS], SetStatus method [VDS],IVdsControllerPort interface, base.ivdscontrollerport_setstatus, vds/IVdsControllerPort::SetStatus, vdshwprv/IVdsControllerPort::SetStatus
f1_keywords:
- vdshwprv/IVdsControllerPort.SetStatus
dev_langs:
- c++
req.header: vdshwprv.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 R2 [desktop apps only]
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
- Vds.h
- VdsHwPrv.h
api_name:
- IVdsControllerPort.SetStatus
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IVdsControllerPort::SetStatus


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://docs.microsoft.com/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Sets the 
   status of a controller port to the specified value.


## -parameters




### -param status

A value enumerated by the <a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/ne-vdshwprv-vds_port_status">VDS_PORT_STATUS</a> enumeration. Passing in 
      <b>VDS_PRS_UNKNOWN</b> fails with <b>E_INVALIDARG</b>.


## -returns



This method can return standard HRESULT values, such as E_INVALIDARG or E_OUTOFMEMORY, and <a href="https://docs.microsoft.com/windows/desktop/VDS/virtual-disk-service-common-return-codes">VDS-specific return values</a>. It can also return converted <a href="https://docs.microsoft.com/windows/desktop/Debug/system-error-codes">system error codes</a>  using the <a href="https://docs.microsoft.com/windows/desktop/api/winerror/nf-winerror-hresult_from_win32">HRESULT_FROM_WIN32</a> macro. Errors can originate from VDS itself or from the underlying <a href="https://docs.microsoft.com/windows/desktop/VDS/about-vds">VDS provider</a> that is being used. Possible return values include the following.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>S_OK</b></b></dt>
</dl>
</td>
<td width="60%">
The status was successfully set.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>VDS_E_PROVIDER_CACHE_CORRUPT</b></b></dt>
<dt>0x8004241FL</dt>
</dl>
</td>
<td width="60%">
The cache of the provider is corrupted. This indicates a software or communication problem inside a provider 
        that caches information about the attached devices. The caller can use the 
        <a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdshwprovider-reenumerate">IVdsHwProvider::Reenumerate</a> method 
        followed by the  <a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdshwprovider-refresh">IVdsHwProvider::Refresh</a> method to 
        restore the cache.
       

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>VDS_E_OBJECT_DELETED</b></b></dt>
<dt>0x8004240BL</dt>
</dl>
</td>
<td width="60%">
The controller port object is no longer present.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>VDS_E_ANOTHER_CALL_IN_PROGRESS</b></b></dt>
<dt>0x80042404L</dt>
</dl>
</td>
<td width="60%">
Another operation is in progress. This operation cannot proceed until previous operations are complete.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>VDS_E_NOT_SUPPORTED</b></b></dt>
<dt>0x80042400L</dt>
</dl>
</td>
<td width="60%">
This operation is not supported by this provider.

</td>
</tr>
</table>
 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdscontrollerport">IVdsControllerPort</a>



<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/ne-vdshwprv-vds_port_status">VDS_PORT_STATUS</a>
 

 

