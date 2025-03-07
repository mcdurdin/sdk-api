---
UID: NF:faxcomex.IFaxRecipients.Add
title: IFaxRecipients::Add (faxcomex.h)
description: The IFaxRecipients::Add method adds a new FaxRecipient object to the FaxRecipients collection.
helpviewer_keywords: ["Add","Add method [Fax Service]","Add method [Fax Service]","IFaxRecipients interface","IFaxRecipients interface [Fax Service]","Add method","IFaxRecipients.Add","IFaxRecipients::Add","_mfax_faxrecipients.add","fax._mfax_faxrecipients_add","fax._mfax_faxrecipients_cpp_mfax_faxrecipients_add_cpp","faxcomex/IFaxRecipients::Add"]
old-location: fax\_mfax_faxrecipients_cpp_mfax_faxrecipients_add_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_73l0.htm
ms.date: 12/05/2018
ms.keywords: Add, Add method [Fax Service], Add method [Fax Service],IFaxRecipients interface, IFaxRecipients interface [Fax Service],Add method, IFaxRecipients.Add, IFaxRecipients::Add, _mfax_faxrecipients.add, fax._mfax_faxrecipients_add, fax._mfax_faxrecipients_cpp_mfax_faxrecipients_add_cpp, faxcomex/IFaxRecipients::Add
f1_keywords:
- faxcomex/IFaxRecipients.Add
dev_langs:
- c++
req.header: faxcomex.h
req.include-header: 
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
req.lib: 
req.dll: Fxscomex.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Fxscomex.dll
api_name:
- IFaxRecipients.Add
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IFaxRecipients::Add


## -description


The <b>IFaxRecipients::Add</b> method adds a new <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxrecipient">FaxRecipient</a> object to the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxrecipients">FaxRecipients</a> collection. 


## -parameters




### -param bstrFaxNumber

Type: <b>BSTR</b>

Specifies the fax number of the fax recipient.


### -param bstrRecipientName [optional]

Type: <b>BSTR</b>

Specifies the name of the fax recipient. 


### -param ppFaxRecipient [out, retval]

Type: <b><a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxrecipient">IFaxRecipient</a>**</b>

A <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxrecipient">FaxRecipient</a> object.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-broadcasting-a-fax">Broadcasting a Fax</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxrecipients">FaxRecipients</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxrecipients">IFaxRecipients</a>
 

 

