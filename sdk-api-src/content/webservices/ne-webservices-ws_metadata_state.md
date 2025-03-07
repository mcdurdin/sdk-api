---
UID: NE:webservices.__unnamed_enum_103
title: WS_METADATA_STATE (webservices.h)
description: The state of the metadata object.
helpviewer_keywords: ["WS_METADATA_STATE","WS_METADATA_STATE enumeration [Web Services for Windows]","WS_METADATA_STATE_CREATED","WS_METADATA_STATE_FAULTED","WS_METADATA_STATE_RESOLVED","webservices/WS_METADATA_STATE","webservices/WS_METADATA_STATE_CREATED","webservices/WS_METADATA_STATE_FAULTED","webservices/WS_METADATA_STATE_RESOLVED","wsw.ws_metadata_state"]
old-location: wsw\ws_metadata_state.htm
tech.root: wsw
ms.assetid: 4d2b8c31-d5ff-4b96-9aaf-57e59d075431
ms.date: 12/05/2018
ms.keywords: WS_METADATA_STATE, WS_METADATA_STATE enumeration [Web Services for Windows], WS_METADATA_STATE_CREATED, WS_METADATA_STATE_FAULTED, WS_METADATA_STATE_RESOLVED, webservices/WS_METADATA_STATE, webservices/WS_METADATA_STATE_CREATED, webservices/WS_METADATA_STATE_FAULTED, webservices/WS_METADATA_STATE_RESOLVED, wsw.ws_metadata_state
f1_keywords:
- webservices/WS_METADATA_STATE
dev_langs:
- c++
req.header: webservices.h
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
- HeaderDef
api_location:
- WebServices.h
api_name:
- WS_METADATA_STATE
targetos: Windows
req.typenames: WS_METADATA_STATE
req.redist: 
ms.custom: 19H1
---

# WS_METADATA_STATE enumeration


## -description


The state of the metadata object.
            


## -enum-fields




### -field WS_METADATA_STATE_CREATED

The initial state of the metadata object.
                


### -field WS_METADATA_STATE_RESOLVED

All references between metadata documents have been
                    resolved and no more metadata documents may be added
                    to the metadata object.  See <a href="https://docs.microsoft.com/windows/desktop/api/webservices/nf-webservices-wsgetmetadataendpoints">WsGetMetadataEndpoints</a> for
                    more information.
                


### -field WS_METADATA_STATE_FAULTED

The metadata object not usable due to a previous error.  See
                    See <a href="https://docs.microsoft.com/windows/desktop/api/webservices/nf-webservices-wsgetmetadataendpoints">WsGetMetadataEndpoints</a> and <a href="https://docs.microsoft.com/windows/desktop/api/webservices/nf-webservices-wsreadmetadata">WsReadMetadata</a>for more information.
                


## -remarks



The following diagram illustrates the functions that 
                cause state transitions in the metadata object.
            

<img alt="" src="./images/MetadataStates.png"/>



