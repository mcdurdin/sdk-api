---
UID: NF:directxcollision.BoundingBox.Intersects(FXMVECTOR,FXMVECTOR,float&)
title: BoundingBox::Intersects(FXMVECTOR,FXMVECTOR,float &)
description: Test the BoundingBox for intersection with a ray.
helpviewer_keywords: ["BoundingBox interface [DirectX Math Support APIs]","Intersects method","BoundingBox.Intersects","BoundingBox.Intersects(FXMVECTOR","FXMVECTOR","float &)","BoundingBox.Intersects(XMVECTOR","XMVECTOR","float&)","BoundingBox::Intersects","BoundingBox::Intersects(FXMVECTOR","FXMVECTOR","float &)","Intersects","Intersects method [DirectX Math Support APIs]","Intersects method [DirectX Math Support APIs]","BoundingBox interface","dxmath.boundingbox_intersects_2"]
old-location: dxmath\boundingbox_intersects_2.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.directxcollision.BoundingBox.Intersects(XMVECTOR,XMVECTOR,float@)
ms.date: 12/05/2018
ms.keywords: BoundingBox interface [DirectX Math Support APIs],Intersects method, BoundingBox.Intersects, BoundingBox.Intersects(FXMVECTOR,FXMVECTOR,float &), BoundingBox.Intersects(XMVECTOR,XMVECTOR,float&), BoundingBox::Intersects, BoundingBox::Intersects(FXMVECTOR,FXMVECTOR,float &), Intersects, Intersects method [DirectX Math Support APIs], Intersects method [DirectX Math Support APIs],BoundingBox interface, dxmath.boundingbox_intersects_2
f1_keywords:
- directxcollision/BoundingBox.Intersects
dev_langs:
- c++
req.header: directxcollision.h
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
req.namespace: Use DirectX.
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
- DirectXCollision.h
api_name:
- BoundingBox.Intersects
targetos: Windows
req.typenames: 
req.redist: 
---

# BoundingBox::Intersects(FXMVECTOR,FXMVECTOR,float &)


## -description


Test the BoundingBox for intersection with a ray.


## -parameters




### -param Origin [in]

The origin of the ray.


### -param Direction [in]

The direction of the ray.


### -param Dist [out, ref]

The length of the ray.


## -returns



A bool value indicating whether the BoundingBox intersects the ray.




## -remarks



<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.




## -see-also




[BoundingBox](/windows/win32/api/directxcollision/ns-directxcollision-boundingbox)



<a href="https://msdn.microsoft.com/df3d3df9-aa74-413d-808c-f7b276d11279">Intersects</a>



<b>Reference</b>
 

 

