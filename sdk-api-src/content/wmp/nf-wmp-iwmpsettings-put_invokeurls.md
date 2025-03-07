---
UID: NF:wmp.IWMPSettings.put_invokeURLs
title: IWMPSettings::put_invokeURLs (wmp.h)
description: The put_invokeURLs method specifies a value indicating whether URL events should launch a Web browser.
helpviewer_keywords: ["IWMPSettings interface [Windows Media Player]","put_invokeURLs method","IWMPSettings.put_invokeURLs","IWMPSettings::put_invokeURLs","IWMPSettingsput_invokeURLs","put_invokeURLs","put_invokeURLs method [Windows Media Player]","put_invokeURLs method [Windows Media Player]","IWMPSettings interface","wmp.iwmpsettings_put_invokeurls","wmp/IWMPSettings::put_invokeURLs"]
old-location: wmp\iwmpsettings_put_invokeurls.htm
tech.root: WMP
ms.assetid: 4c62ba8e-8fca-4cfe-9a52-6b6ac2c7c0de
ms.date: 12/05/2018
ms.keywords: IWMPSettings interface [Windows Media Player],put_invokeURLs method, IWMPSettings.put_invokeURLs, IWMPSettings::put_invokeURLs, IWMPSettingsput_invokeURLs, put_invokeURLs, put_invokeURLs method [Windows Media Player], put_invokeURLs method [Windows Media Player],IWMPSettings interface, wmp.iwmpsettings_put_invokeurls, wmp/IWMPSettings::put_invokeURLs
f1_keywords:
- wmp/IWMPSettings.put_invokeURLs
dev_langs:
- c++
req.header: wmp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Media Player 9 Series or later.
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
req.dll: Wmp.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- wmp.dll
api_name:
- IWMPSettings.put_invokeURLs
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMPSettings::put_invokeURLs


## -description



The <b>put_invokeURLs</b> method specifies a value indicating whether URL events should launch a Web browser.




## -parameters




### -param fInvokeURLs [in]

<b>VARIANT_BOOL</b> indicating whether URL events should launch a Web browser. The default is <b>TRUE</b>.


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
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
</table>
 




## -remarks



Digital media files and streams can contain URL script commands. When a URL script command is sent to the Windows Media Player control, it is passed first to the <b>ScriptCommand</b> event handler regardless of the value specified in <b>put_invokeURLs</b>. After <b>ScriptCommand</b> exits, Windows Media Player checks the <b>VARIANT_BOOL</b> specified in <b>put_invokeURLs</b> to determine whether to launch the default Web browser with the URL. You can selectively display URLs by checking them in <b>ScriptCommand</b> and setting <b>put_invokeURLs</b> as needed.

<b>Windows Media Player 10 Mobile:</b> This method only accepts a <b>VARIANT_BOOL</b> set to <b>FALSE</b>, otherwise an E_INVALIDARG <b>HRESULT</b> is returned.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpevents-scriptcommand">IWMPEvents::ScriptCommand</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nn-wmp-iwmpsettings">IWMPSettings Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpsettings-get_invokeurls">IWMPSettings::get_invokeURLs</a>
 

 

