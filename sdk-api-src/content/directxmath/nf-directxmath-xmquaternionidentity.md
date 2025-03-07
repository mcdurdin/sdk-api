---
UID: NF:directxmath.XMQuaternionIdentity
title: XMQuaternionIdentity function (directxmath.h)
description: Returns the identity quaternion.
helpviewer_keywords: ["Use DirectX..XMQuaternionIdentity","XMQuaternionIdentity","XMQuaternionIdentity method [DirectX Math Support APIs]","dxmath.xmquaternionidentity"]
old-location: dxmath\xmquaternionidentity.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.quaternion.XMQuaternionIdentity
ms.date: 12/05/2018
ms.keywords: Use DirectX..XMQuaternionIdentity, XMQuaternionIdentity, XMQuaternionIdentity method [DirectX Math Support APIs], dxmath.xmquaternionidentity
f1_keywords:
- directxmath/XMQuaternionIdentity
dev_langs:
- c++
req.header: directxmath.h
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
- DirectXMath.h
api_name:
- XMQuaternionIdentity
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# XMQuaternionIdentity function


## -description


Returns the identity quaternion.


## -parameters






## -returns



An <a href="https://docs.microsoft.com/windows/desktop/dxmath/xmvector-data-type">XMVECTOR</a> union that is the identity quaternion.




## -remarks



The DirectXMath quaternion functions use an XMVECTOR 4-vector to represent quaternions, 
    where the X, Y, and Z components are the vector part and the W component is the scalar part.

Given a quaternion (x, y, z, w), the <code>XMQuaternionIdentity</code> function will return the quaternion (0, 0, 0, 1).

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/dxmath/ovw-xnamath-reference-functions-quaternion">DirectXMath Library Quaternion Functions</a>
 

 

