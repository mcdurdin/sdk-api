---
UID: NF:dxvahd.IDXVAHD_VideoProcessor.SetVideoProcessStreamState
title: IDXVAHD_VideoProcessor::SetVideoProcessStreamState (dxvahd.h)
description: Sets a state parameter for an input stream on a Microsoft DirectX Video Acceleration High Definition (DXVA-HD) device.
helpviewer_keywords: ["IDXVAHD_VideoProcessor interface [Media Foundation]","SetVideoProcessStreamState method","IDXVAHD_VideoProcessor.SetVideoProcessStreamState","IDXVAHD_VideoProcessor::SetVideoProcessStreamState","SetVideoProcessStreamState","SetVideoProcessStreamState method [Media Foundation]","SetVideoProcessStreamState method [Media Foundation]","IDXVAHD_VideoProcessor interface","dxvahd/IDXVAHD_VideoProcessor::SetVideoProcessStreamState","mf.idxvahd_videoprocessor_setvideoprocessstreamstate"]
old-location: mf\idxvahd_videoprocessor_setvideoprocessstreamstate.htm
tech.root: mf
ms.assetid: 40a8444f-576e-40ff-804e-0912812f0ee6
ms.date: 12/05/2018
ms.keywords: IDXVAHD_VideoProcessor interface [Media Foundation],SetVideoProcessStreamState method, IDXVAHD_VideoProcessor.SetVideoProcessStreamState, IDXVAHD_VideoProcessor::SetVideoProcessStreamState, SetVideoProcessStreamState, SetVideoProcessStreamState method [Media Foundation], SetVideoProcessStreamState method [Media Foundation],IDXVAHD_VideoProcessor interface, dxvahd/IDXVAHD_VideoProcessor::SetVideoProcessStreamState, mf.idxvahd_videoprocessor_setvideoprocessstreamstate
f1_keywords:
- dxvahd/IDXVAHD_VideoProcessor.SetVideoProcessStreamState
dev_langs:
- c++
req.header: dxvahd.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
- dxvahd.h
api_name:
- IDXVAHD_VideoProcessor.SetVideoProcessStreamState
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDXVAHD_VideoProcessor::SetVideoProcessStreamState


## -description


Sets a state parameter for an input stream on a  Microsoft DirectX Video Acceleration High Definition (DXVA-HD) device.


## -parameters




### -param StreamNumber [in]

The zero-based index of the input stream. To get the maximum number of streams, call <a href="https://docs.microsoft.com/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-getvideoprocessordevicecaps">IDXVAHD_Device::GetVideoProcessorDeviceCaps</a> and check the <b>MaxStreamStates</b> member of the <a href="https://docs.microsoft.com/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpdevcaps">DXVAHD_VPDEVCAPS</a> structure.


### -param State [in]

The state parameter to set, specified as a member of the <a href="https://docs.microsoft.com/windows/desktop/api/dxvahd/ne-dxvahd-dxvahd_stream_state">DXVAHD_STREAM_STATE</a> enumeration.


### -param DataSize [in]

The size, in bytes, of the buffer pointed to by <i>pData</i>.


### -param pData [in]

A pointer to a buffer that contains the state data. The meaning of the data depends on the <i>State</i> parameter. Each state has a corresponding data structure; for more information, see <a href="https://docs.microsoft.com/windows/desktop/api/dxvahd/ne-dxvahd-dxvahd_stream_state">DXVAHD_STREAM_STATE</a>. The caller allocates the buffer and fills in the parameter data before calling this method.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Call this method to set state parameters that apply to individual input streams. 
      




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/dxva-hd">DXVA-HD</a>



<a href="https://docs.microsoft.com/windows/desktop/api/dxvahd/nn-dxvahd-idxvahd_videoprocessor">IDXVAHD_VideoProcessor</a>
 

 

