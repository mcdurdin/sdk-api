---
UID: NE:d2d1effects.D2D1_SCALE_INTERPOLATION_MODE
title: D2D1_SCALE_INTERPOLATION_MODE (d2d1effects.h)
description: The interpolation mode the Scale effect uses to scale the image. There are 6 scale modes that range in quality and speed.
helpviewer_keywords: ["D2D1_SCALE_INTERPOLATION_MODE","D2D1_SCALE_INTERPOLATION_MODE enumeration [Direct2D]","D2D1_SCALE_INTERPOLATION_MODE_ANISOTROPIC","D2D1_SCALE_INTERPOLATION_MODE_CUBIC","D2D1_SCALE_INTERPOLATION_MODE_HIGH_QUALITY_CUBIC","D2D1_SCALE_INTERPOLATION_MODE_LINEAR","D2D1_SCALE_INTERPOLATION_MODE_MULTI_SAMPLE_LINEAR","D2D1_SCALE_INTERPOLATION_MODE_NEAREST_NEIGHBOR","d2d1effects/D2D1_SCALE_INTERPOLATION_MODE","d2d1effects/D2D1_SCALE_INTERPOLATION_MODE_ANISOTROPIC","d2d1effects/D2D1_SCALE_INTERPOLATION_MODE_CUBIC","d2d1effects/D2D1_SCALE_INTERPOLATION_MODE_HIGH_QUALITY_CUBIC","d2d1effects/D2D1_SCALE_INTERPOLATION_MODE_LINEAR","d2d1effects/D2D1_SCALE_INTERPOLATION_MODE_MULTI_SAMPLE_LINEAR","d2d1effects/D2D1_SCALE_INTERPOLATION_MODE_NEAREST_NEIGHBOR","direct2d.d2d1_scale_interpolation_mode"]
old-location: direct2d\d2d1_scale_interpolation_mode.htm
tech.root: Direct2D
ms.assetid: 2673E6AE-EEF5-4727-B224-0245CED15C21
ms.date: 12/05/2018
ms.keywords: D2D1_SCALE_INTERPOLATION_MODE, D2D1_SCALE_INTERPOLATION_MODE enumeration [Direct2D], D2D1_SCALE_INTERPOLATION_MODE_ANISOTROPIC, D2D1_SCALE_INTERPOLATION_MODE_CUBIC, D2D1_SCALE_INTERPOLATION_MODE_HIGH_QUALITY_CUBIC, D2D1_SCALE_INTERPOLATION_MODE_LINEAR, D2D1_SCALE_INTERPOLATION_MODE_MULTI_SAMPLE_LINEAR, D2D1_SCALE_INTERPOLATION_MODE_NEAREST_NEIGHBOR, d2d1effects/D2D1_SCALE_INTERPOLATION_MODE, d2d1effects/D2D1_SCALE_INTERPOLATION_MODE_ANISOTROPIC, d2d1effects/D2D1_SCALE_INTERPOLATION_MODE_CUBIC, d2d1effects/D2D1_SCALE_INTERPOLATION_MODE_HIGH_QUALITY_CUBIC, d2d1effects/D2D1_SCALE_INTERPOLATION_MODE_LINEAR, d2d1effects/D2D1_SCALE_INTERPOLATION_MODE_MULTI_SAMPLE_LINEAR, d2d1effects/D2D1_SCALE_INTERPOLATION_MODE_NEAREST_NEIGHBOR, direct2d.d2d1_scale_interpolation_mode
f1_keywords:
- d2d1effects/D2D1_SCALE_INTERPOLATION_MODE
dev_langs:
- c++
req.header: d2d1effects.h
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
- HeaderDef
api_location:
- d2d1effects.h
api_name:
- D2D1_SCALE_INTERPOLATION_MODE
targetos: Windows
req.typenames: D2D1_SCALE_INTERPOLATION_MODE
req.redist: 
ms.custom: 19H1
---

# D2D1_SCALE_INTERPOLATION_MODE enumeration


## -description


The interpolation mode the <a href="https://docs.microsoft.com/windows/desktop/Direct2D/high-quality-scale">Scale effect</a> uses to scale the image. There are 6 scale modes that range in quality and speed. 


## -enum-fields




### -field D2D1_SCALE_INTERPOLATION_MODE_NEAREST_NEIGHBOR

Samples the nearest single point and uses that. This mode uses less processing time, but outputs the lowest quality image.


### -field D2D1_SCALE_INTERPOLATION_MODE_LINEAR

Uses a four point sample and linear interpolation. This mode uses more processing time than the nearest neighbor mode, but outputs a higher quality image.


### -field D2D1_SCALE_INTERPOLATION_MODE_CUBIC

Uses a 16 sample cubic kernel for interpolation. This mode uses the most processing time, but outputs a higher quality image. 


### -field D2D1_SCALE_INTERPOLATION_MODE_MULTI_SAMPLE_LINEAR

Uses 4 linear samples within a single pixel for good edge anti-aliasing. This mode is good for scaling down by small amounts on images with few pixels.


### -field D2D1_SCALE_INTERPOLATION_MODE_ANISOTROPIC

Uses anisotropic filtering to sample a pattern according to the transformed shape of the bitmap.


### -field D2D1_SCALE_INTERPOLATION_MODE_HIGH_QUALITY_CUBIC

Uses a variable size high quality cubic kernel to perform a pre-downscale the image if downscaling is involved in the transform matrix. Then uses the cubic interpolation mode for the final output.


### -field D2D1_SCALE_INTERPOLATION_MODE_FORCE_DWORD



