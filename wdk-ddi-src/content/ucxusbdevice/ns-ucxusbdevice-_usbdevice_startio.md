---
UID: NS:ucxusbdevice._USBDEVICE_STARTIO
title: _USBDEVICE_STARTIO (ucxusbdevice.h)
description: Contains a handle for the Universal Serial Bus (USB) hub or device on which to start data transfer.
old-location: buses\_usbdevice_startio.htm
tech.root: usbref
ms.date: 05/07/2018
keywords: ["USBDEVICE_STARTIO structure"]
ms.keywords: "*PUSBDEVICE_STARTIO, P_USBDEVICE_STARTIO, P_USBDEVICE_STARTIO structure pointer [Buses], USBDEVICE_STARTIO, USBDEVICE_STARTIO structure [Buses], _USBDEVICE_STARTIO, buses._usbdevice_startio, ucxusbdevice/P_USBDEVICE_STARTIO, ucxusbdevice/_USBDEVICE_STARTIO"
req.header: ucxusbdevice.h
req.include-header: Ucxclass.h
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
req.typenames: USBDEVICE_STARTIO, *PUSBDEVICE_STARTIO
f1_keywords:
 - _USBDEVICE_STARTIO
 - ucxusbdevice/_USBDEVICE_STARTIO
 - PUSBDEVICE_STARTIO
 - ucxusbdevice/PUSBDEVICE_STARTIO
 - USBDEVICE_STARTIO
 - ucxusbdevice/USBDEVICE_STARTIO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ucxusbdevice.h
api_name:
 - USBDEVICE_STARTIO
---

# _USBDEVICE_STARTIO structure


## -description

Contains a handle for the Universal Serial Bus (USB) hub or device on which to start data transfer.

## -struct-fields

### -field Header

A <a href="/windows-hardware/drivers/ddi/ucxusbdevice/ns-ucxusbdevice-_usbdevice_mgmt_header">USBDEVICE_MGMT_HEADER</a> structure that contains  the handle for the USB hub or device.

## -see-also

<a href="/windows-hardware/drivers/ddi/ucxusbdevice/ns-ucxusbdevice-_usbdevice_abortio">USBDEVICE_ABORTIO</a>



<a href="/windows-hardware/drivers/ddi/ucxusbdevice/ns-ucxusbdevice-_usbdevice_purgeio">USBDEVICE_PURGEIO</a>
