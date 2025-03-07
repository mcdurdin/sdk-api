---
UID: NF:refptrco.TRefPointerCollection.BeginEnum
title: TRefPointerCollection::BeginEnum (refptrco.h)
description: The BeginEnum method starts enumerating the collection.
helpviewer_keywords: ["BeginEnum","BeginEnum method [Windows Management Instrumentation]","BeginEnum method [Windows Management Instrumentation]","TRefPointerCollection interface","TRefPointerCollection interface [Windows Management Instrumentation]","BeginEnum method","TRefPointerCollection.BeginEnum","TRefPointerCollection::BeginEnum","_hmm_trefpointercollection_beginenum","refptrco/TRefPointerCollection::BeginEnum","wmi.trefpointercollection_beginenum"]
old-location: wmi\trefpointercollection_beginenum.htm
tech.root: wmi
ms.assetid: 5f7879e8-0eeb-4768-a478-8effd4e355d3
ms.date: 12/05/2018
ms.keywords: BeginEnum, BeginEnum method [Windows Management Instrumentation], BeginEnum method [Windows Management Instrumentation],TRefPointerCollection interface, TRefPointerCollection interface [Windows Management Instrumentation],BeginEnum method, TRefPointerCollection.BeginEnum, TRefPointerCollection::BeginEnum, _hmm_trefpointercollection_beginenum, refptrco/TRefPointerCollection::BeginEnum, wmi.trefpointercollection_beginenum
f1_keywords:
- refptrco/TRefPointerCollection.BeginEnum
dev_langs:
- c++
req.header: refptrco.h
req.include-header: FwCommon.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: FrameDyn.lib
req.dll: FrameDynOS.dll; FrameDyn.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- FrameDynOS.dll
- FrameDyn.dll
api_name:
- TRefPointerCollection.BeginEnum
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# TRefPointerCollection::BeginEnum


## -description


<p class="CCE_Message">[The <a href="https://docs.microsoft.com/windows/desktop/api/refptrco/nl-refptrco-trefpointercollection">TRefPointerCollection</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="https://docs.microsoft.com/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure">MI APIs</a> should be used for all new 
    development.]

The <b>BeginEnum</b> method starts enumerating the collection.


## -parameters




### -param pos [ref]

Denotes the position of an item in a collection of <a href="https://docs.microsoft.com/windows/desktop/api/refptrco/nl-refptrco-trefpointercollection">TRefPointerCollection</a> objects.


## -returns



If the method is successful, it returns <b>TRUE</b>.

If the method fails, it returns <b>FALSE</b>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/refptrco/nl-refptrco-trefpointercollection">TRefPointerCollection</a>



<a href="https://docs.microsoft.com/windows/desktop/api/refptrco/nf-refptrco-trefpointercollection-endenum">TRefPointerCollection::EndEnum</a>
 

 

