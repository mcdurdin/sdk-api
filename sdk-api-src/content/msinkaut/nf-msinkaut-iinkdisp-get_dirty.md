---
UID: NF:msinkaut.IInkDisp.get_Dirty
title: IInkDisp::get_Dirty (msinkaut.h)
description: Gets or sets the value that specifies whether the strokes of an InkDisp Class object have been modified since the last time the ink was saved.
helpviewer_keywords: ["3399219f-96a5-4c66-8e41-89927ea1020d","Dirty property [Tablet PC]","Dirty property [Tablet PC]","IInkDisp interface","IInkDisp interface [Tablet PC]","Dirty property","IInkDisp.Dirty","IInkDisp.get_Dirty","IInkDisp::Dirty","IInkDisp::get_Dirty","IInkDisp::put_Dirty","InkDisp.get_Dirty","InkDisp.put_Dirty","get_Dirty","msinkaut/IInkDisp::Dirty","msinkaut/IInkDisp::get_Dirty","msinkaut/IInkDisp::put_Dirty","put_Dirty","tablet.inkdisp_dirty"]
old-location: tablet\inkdisp_dirty.htm
tech.root: tablet
ms.assetid: 3399219f-96a5-4c66-8e41-89927ea1020d
ms.date: 12/05/2018
ms.keywords: 3399219f-96a5-4c66-8e41-89927ea1020d, Dirty property [Tablet PC], Dirty property [Tablet PC],IInkDisp interface, IInkDisp interface [Tablet PC],Dirty property, IInkDisp.Dirty, IInkDisp.get_Dirty, IInkDisp::Dirty, IInkDisp::get_Dirty, IInkDisp::put_Dirty, InkDisp.get_Dirty, InkDisp.put_Dirty, get_Dirty, msinkaut/IInkDisp::Dirty, msinkaut/IInkDisp::get_Dirty, msinkaut/IInkDisp::put_Dirty, put_Dirty, tablet.inkdisp_dirty
f1_keywords:
- msinkaut/IInkDisp.Dirty
dev_langs:
- c++
req.header: msinkaut.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP Tablet PC Edition [desktop apps only]
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
req.lib: InkObj.dll
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- InkObj.dll
- InkObj.dll.dll
api_name:
- IInkDisp.Dirty
- IInkDisp.get_Dirty
- IInkDisp.put_Dirty
- InkDisp.get_Dirty
- InkDisp.put_Dirty
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IInkDisp::get_Dirty


## -description



Gets or sets the value that specifies whether the strokes of an <a href="https://docs.microsoft.com/windows/desktop/tablet/inkdisp-class">InkDisp Class</a> object have been modified since the last time the ink was saved.



This property is read/write.


## -parameters


## -remarks



After ink is saved, the dirty flag is automatically cleared and the value of this property is <b>VARIANT_FALSE</b>. To save ink, call the <a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-save">Save Method</a> method.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Mt846797(v=VS.85).aspx">IInkDisp</a>



<a href="https://docs.microsoft.com/windows/desktop/tablet/inkdisp-class">InkDisp Class</a>



<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-save">Save Method</a>
 

 

