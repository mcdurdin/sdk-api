---
UID: NF:directxmath.XMVector3TransformNormalStream
title: XMVector3TransformNormalStream function (directxmath.h)
description: Transforms a stream of 3D normal vectors by a given matrix.
helpviewer_keywords: ["Use DirectX..XMVector3TransformNormalStream","XMVector3TransformNormalStream","XMVector3TransformNormalStream method [DirectX Math Support APIs]","dxmath.xmvector3transformnormalstream"]
old-location: dxmath\xmvector3transformnormalstream.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.transformation.XMVector3TransformNormalStream(XMFLOAT3@,size_t,const XMFLOAT3,size_t,size_t,XMMATRIX)
ms.date: 12/05/2018
ms.keywords: Use DirectX..XMVector3TransformNormalStream, XMVector3TransformNormalStream, XMVector3TransformNormalStream method [DirectX Math Support APIs], dxmath.xmvector3transformnormalstream
f1_keywords:
- directxmath/XMVector3TransformNormalStream
dev_langs:
- c++
req.header: directxmath.h
req.include-header: DirectXMath.h
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
- directxmathvector.inl
api_name:
- XMVector3TransformNormalStream
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# XMVector3TransformNormalStream function


## -description


Transforms a stream of 3D normal vectors by a given matrix.


## -parameters




### -param pOutputStream [out]

Address of the first <a href="https://docs.microsoft.com/windows/desktop/api/directxmath/ns-directxmath-xmfloat3">XMFLOAT3</a> in the destination stream.


### -param OutputStride [in]

Stride, in bytes, between vectors in the destination stream.


### -param pInputStream [in]

Address of the first <a href="https://docs.microsoft.com/windows/desktop/api/directxmath/ns-directxmath-xmfloat3">XMFLOAT3</a> in the stream to be transformed.


### -param InputStride [in]

Stride, in bytes, between vectors in the input stream.


### -param VectorCount [in]

Number of vectors to transform.


### -param M [in]

Transformation matrix.


## -returns



Returns the address of the first <a href="https://docs.microsoft.com/windows/desktop/api/directxmath/ns-directxmath-xmfloat3">XMFLOAT3</a> in the destination stream.




## -remarks



Each vector in the input stream must be normalized.

<code>XMVector3TransformNormalStream</code> performs transformations using the input matrix rows 0, 1, and 2 for rotation and scaling, and ignores row 3.

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/dxmath/ovw-xnamath-reference-functions-vector3-transformation">DirectXMath Library 3D Vector Transformation Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/api/directxmath/nf-directxmath-xmvector3transformnormal">XMVector3TransformNormal</a>
 

 

