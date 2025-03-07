---
UID: NF:dvbsiparser.IDVB_BAT.GetBouquetId
title: IDVB_BAT::GetBouquetId (dvbsiparser.h)
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
helpviewer_keywords: ["GetBouquetId","GetBouquetId method [Microsoft TV Technologies]","GetBouquetId method [Microsoft TV Technologies]","IDVB_BAT interface","IDVB_BAT interface [Microsoft TV Technologies]","GetBouquetId method","IDVB_BAT.GetBouquetId","IDVB_BAT::GetBouquetId","IDVB_BATGetBouquetId","dvbsiparser/IDVB_BAT::GetBouquetId","mstv.idvb_bat_getbouquetid"]
old-location: mstv\idvb_bat_getbouquetid.htm
tech.root: mstv
ms.assetid: 43c8d96d-24a7-459b-8221-daef7759c603
ms.date: 12/05/2018
ms.keywords: GetBouquetId, GetBouquetId method [Microsoft TV Technologies], GetBouquetId method [Microsoft TV Technologies],IDVB_BAT interface, IDVB_BAT interface [Microsoft TV Technologies],GetBouquetId method, IDVB_BAT.GetBouquetId, IDVB_BAT::GetBouquetId, IDVB_BATGetBouquetId, dvbsiparser/IDVB_BAT::GetBouquetId, mstv.idvb_bat_getbouquetid
f1_keywords:
- dvbsiparser/IDVB_BAT.GetBouquetId
dev_langs:
- c++
req.header: dvbsiparser.h
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
- dvbsiparser.h
api_name:
- IDVB_BAT.GetBouquetId
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDVB_BAT::GetBouquetId


## -description



This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        



The <b>GetBouquetId</b> method returns the bouquet identifier for the BAT.


## -parameters




### -param pwVal [out]

Pointer to a variable that receives the bouquet_id field.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
NULL pointer argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MPEG2_E_UNDEFINED</b></dt>
</dl>
</td>
<td width="60%">
The table does not contain this field.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
</table>
 




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-idvb_bat">IDVB_BAT Interface</a>
 

 

