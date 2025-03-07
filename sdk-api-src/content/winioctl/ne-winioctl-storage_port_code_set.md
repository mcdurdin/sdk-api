---
UID: NE:winioctl._STORAGE_PORT_CODE_SET
title: STORAGE_PORT_CODE_SET
description: Reserved for system use.
helpviewer_keywords: ["*PSTORAGE_PORT_CODE_SET","PSTORAGE_PORT_CODE_SET","PSTORAGE_PORT_CODE_SET enumeration pointer [Files]","STORAGE_PORT_CODE_SET","STORAGE_PORT_CODE_SET enumeration [Files]","StoragePortCodeSetATAport","StoragePortCodeSetReserved","StoragePortCodeSetSBP2port","StoragePortCodeSetSCSIport","StoragePortCodeSetSDport","StoragePortCodeSetSpaceport","StoragePortCodeSetStorport","StoragePortCodeSetUSBport","fs.storage_port_code_set","winioctl/PSTORAGE_PORT_CODE_SET","winioctl/STORAGE_PORT_CODE_SET","winioctl/StoragePortCodeSetATAport","winioctl/StoragePortCodeSetReserved","winioctl/StoragePortCodeSetSBP2port","winioctl/StoragePortCodeSetSCSIport","winioctl/StoragePortCodeSetSDport","winioctl/StoragePortCodeSetSpaceport","winioctl/StoragePortCodeSetStorport","winioctl/StoragePortCodeSetUSBport"]
old-location: fs\storage_port_code_set.htm
tech.root: fs
ms.assetid: 1c1032e8-30b8-45ad-973a-c7616139b26e
ms.date: 12/05/2018
ms.keywords: '*PSTORAGE_PORT_CODE_SET, PSTORAGE_PORT_CODE_SET, PSTORAGE_PORT_CODE_SET enumeration pointer [Files], STORAGE_PORT_CODE_SET, STORAGE_PORT_CODE_SET enumeration [Files], StoragePortCodeSetATAport, StoragePortCodeSetReserved, StoragePortCodeSetSBP2port, StoragePortCodeSetSCSIport, StoragePortCodeSetSDport, StoragePortCodeSetSpaceport, StoragePortCodeSetStorport, StoragePortCodeSetUSBport, fs.storage_port_code_set, winioctl/PSTORAGE_PORT_CODE_SET, winioctl/STORAGE_PORT_CODE_SET, winioctl/StoragePortCodeSetATAport, winioctl/StoragePortCodeSetReserved, winioctl/StoragePortCodeSetSBP2port, winioctl/StoragePortCodeSetSCSIport, winioctl/StoragePortCodeSetSDport, winioctl/StoragePortCodeSetSpaceport, winioctl/StoragePortCodeSetStorport, winioctl/StoragePortCodeSetUSBport'
f1_keywords:
- winioctl/STORAGE_PORT_CODE_SET
dev_langs:
- c++
req.header: winioctl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
- WinIoCtl.h
api_name:
- STORAGE_PORT_CODE_SET
targetos: Windows
req.typenames: STORAGE_PORT_CODE_SET, *PSTORAGE_PORT_CODE_SET
req.redist: 
---

# STORAGE_PORT_CODE_SET enumeration

## -description

Reserved for system use. 


## -enum-fields

### -field StoragePortCodeSetReserved

Indicates an unknown storage adapter driver type.


### -field StoragePortCodeSetStorport

Storage adapter driver is a Storport-miniport driver.


### -field StoragePortCodeSetSCSIport

Storage adapter driver is a SCSI Port-miniport driver.


### -field StoragePortCodeSetSpaceport

Storage adapter driver is the Spaceport driver.


### -field StoragePortCodeSetATAport

Storage adapter driver is an ATA-port miniport driver.


### -field StoragePortCodeSetUSBport

Storage adapter driver is the  USB-storage port driver.


### -field StoragePortCodeSetSBP2port

Storage adapter driver is the  SBP2 port driver.


### -field StoragePortCodeSetSDport

Storage adapter driver is an SD-port miniport driver.


## -see-also

* [Disk Management Enumeration Types](https://docs.microsoft.com/windows/desktop/FileIO/disk-management-enumeration-types)
* [STORAGE_MINIPORT_DESCRIPTOR](ns-winioctl-storage_miniport_descriptor.md)
