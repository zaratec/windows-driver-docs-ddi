---
UID: NS:ntddcdvd._DVD_DISK_KEY_DESCRIPTOR
title: _DVD_DISK_KEY_DESCRIPTOR (ntddcdvd.h)
description: The DVD_DISK_KEY_DESCRIPTOR structure is used in conjunction with the IOCTL_DVD_READ_STRUCTURE request to retrieve a DVD disc key descriptor.
old-location: storage\dvd_disk_key_descriptor.htm
tech.root: storage
ms.date: 03/29/2018
keywords: ["DVD_DISK_KEY_DESCRIPTOR structure"]
ms.keywords: "*PDVD_DISK_KEY_DESCRIPTOR, DVD_DISK_KEY_DESCRIPTOR, DVD_DISK_KEY_DESCRIPTOR structure [Storage Devices], PDVD_DISK_KEY_DESCRIPTOR, PDVD_DISK_KEY_DESCRIPTOR structure pointer [Storage Devices], _DVD_DISK_KEY_DESCRIPTOR, ntddcdvd/DVD_DISK_KEY_DESCRIPTOR, ntddcdvd/PDVD_DISK_KEY_DESCRIPTOR, storage.dvd_disk_key_descriptor, structs-DVD_b5c88389-0128-4069-b460-d9fa81a2150e.xml"
req.header: ntddcdvd.h
req.include-header: Ntddcdvd.h
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
targetos: Windows
req.typenames: DVD_DISK_KEY_DESCRIPTOR, *PDVD_DISK_KEY_DESCRIPTOR
f1_keywords:
 - _DVD_DISK_KEY_DESCRIPTOR
 - ntddcdvd/_DVD_DISK_KEY_DESCRIPTOR
 - PDVD_DISK_KEY_DESCRIPTOR
 - ntddcdvd/PDVD_DISK_KEY_DESCRIPTOR
 - DVD_DISK_KEY_DESCRIPTOR
 - ntddcdvd/DVD_DISK_KEY_DESCRIPTOR
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ntddcdvd.h
api_name:
 - DVD_DISK_KEY_DESCRIPTOR
---

# _DVD_DISK_KEY_DESCRIPTOR structure


## -description

The DVD_DISK_KEY_DESCRIPTOR structure is used in conjunction with the <a href="/windows-hardware/drivers/ddi/ntddcdvd/ni-ntddcdvd-ioctl_dvd_read_structure">IOCTL_DVD_READ_STRUCTURE</a> request to retrieve a DVD disc key descriptor.

## -struct-fields

### -field DiskKeyData

Pointer to a buffer containing the disc key data obfuscated by the bus key.

## -see-also

<a href="/windows-hardware/drivers/ddi/ntddcdvd/ni-ntddcdvd-ioctl_dvd_read_structure">IOCTL_DVD_READ_STRUCTURE</a>
