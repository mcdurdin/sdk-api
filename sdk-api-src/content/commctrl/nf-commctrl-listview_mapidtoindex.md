---
UID: NF:commctrl.ListView_MapIDToIndex
title: ListView_MapIDToIndex macro (commctrl.h)
description: Maps the ID of an item to an index. You can use this macro or send the LVM_MAPIDTOINDEX message explicitly.
helpviewer_keywords: ["ListView_MapIDToIndex","ListView_MapIDToIndex macro [Windows Controls]","_win32_ListView_MapIDToIndex","_win32_ListView_MapIDToIndex_cpp","commctrl/ListView_MapIDToIndex","controls.ListView_MapIDToIndex","controls._win32_ListView_MapIDToIndex"]
old-location: controls\ListView_MapIDToIndex.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_mapidtoindex.htm
ms.date: 12/05/2018
ms.keywords: ListView_MapIDToIndex, ListView_MapIDToIndex macro [Windows Controls], _win32_ListView_MapIDToIndex, _win32_ListView_MapIDToIndex_cpp, commctrl/ListView_MapIDToIndex, controls.ListView_MapIDToIndex, controls._win32_ListView_MapIDToIndex
f1_keywords:
- commctrl/ListView_MapIDToIndex
dev_langs:
- c++
req.header: commctrl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
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
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- Commctrl.h
api_name:
- ListView_MapIDToIndex
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ListView_MapIDToIndex macro


## -description


Maps the ID of an item to an index. You can use this macro or send the <a href="https://docs.microsoft.com/windows/desktop/controls/lvm-mapidtoindex">LVM_MAPIDTOINDEX</a> message explicitly. 


## -parameters




### -param hwnd

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the list-view control. 


### -param id

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">UINT</a></b>

A <b>UINT</b> that contains the unique ID of an item.


## -remarks



List-view controls internally track items by index. This can present problems because indexes can change during the control's existence.

You can use this macro to tag an item with an ID when you create the item.
You use this ID to guarantee uniqueness during the existence of the list-view control.   
		

To uniquely identify an item, take the index that returns from a call, such as <a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-icomponent-getdisplayinfo">IComponent::GetDisplayInfo</a>, and call <a href="https://docs.microsoft.com/windows/desktop/Controls/lvm-mapindextoid">LVM_MAPINDEXTOID</a>. The return value is a unique ID.
		

If you need to know the index of an item after creating an ID, call
<a href="https://docs.microsoft.com/windows/desktop/controls/lvm-mapidtoindex">LVM_MAPIDTOINDEX</a> with the unique ID and it returns the most current index.

<div class="alert"><b>Note</b>  In a multithreaded environment, you can only be sure the correct index is returned
on the thread that hosts the list-view control, not on background threads.</div>
<div> </div>
To use <b>ListView_MapIDToIndex</b>, specify Comctl32.dll version 6 in the manifest. For more information on manifests, see <a href="https://docs.microsoft.com/windows/desktop/Controls/cookbook-overview">Enabling Visual Styles</a>. 



