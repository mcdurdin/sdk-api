---
UID: NN:shobjidl.IHWEventHandler2
title: IHWEventHandler2 (shobjidl.h)
description: Extends the IHWEventHandler interface to address User Account Control (UAC) elevation for device handlers.
helpviewer_keywords: ["IHWEventHandler2","IHWEventHandler2 interface [Windows Shell]","IHWEventHandler2 interface [Windows Shell]","described","_shell_IHWEventHandler2","shell.IHWEventHandler2","shobjidl/IHWEventHandler2"]
old-location: shell\IHWEventHandler2.htm
tech.root: shell
ms.assetid: 2885bce8-3139-4158-b178-d36bb13aff0f
ms.date: 12/05/2018
ms.keywords: IHWEventHandler2, IHWEventHandler2 interface [Windows Shell], IHWEventHandler2 interface [Windows Shell],described, _shell_IHWEventHandler2, shell.IHWEventHandler2, shobjidl/IHWEventHandler2
f1_keywords:
- shobjidl/IHWEventHandler2
dev_langs:
- c++
req.header: shobjidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Shell32.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Shell32.dll
api_name:
- IHWEventHandler2
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IHWEventHandler2 interface


## -description


Extends the <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl/nn-shobjidl-ihweventhandler">IHWEventHandler</a> interface to address User Account Control (UAC) elevation for device handlers.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IHWEventHandler2</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl/nn-shobjidl-ihweventhandler">IHWEventHandler</a>. <b>IHWEventHandler2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IHWEventHandler2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl/nf-shobjidl-ihweventhandler2-handleeventwithhwnd">HandleEventWithHWND</a>
</td>
<td align="left" width="63%">
Handles AutoPlay device events that contain content types that the application is not registered to handle. This method provides a handle to the owner window so that UI can be displayed if the process requires elevated privileges.

</td>
</tr>
</table> 


## -remarks



This interface also provides the methods of the <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl/nn-shobjidl-ihweventhandler">IHWEventHandler</a> interface, from which it inherits.

Handlers that implement this interface should return quickly from calls to <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl/nf-shobjidl-ihweventhandler-handleevent">IHWEventHandler::HandleEvent</a> and <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl/nf-shobjidl-ihweventhandler2-handleeventwithhwnd">IHWEventHandler2::HandleEventWithHWND</a> so they do not block the AutoPlay dialog from closing. Also, if a local server must be launched for the creation of this handler, it should not block the CreateInstance call; it should return as soon as possible.



