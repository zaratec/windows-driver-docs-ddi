---
UID: NS:hbapiwmi._GetFcpPersistentBinding_IN
title: _GetFcpPersistentBinding_IN (hbapiwmi.h)
description: The GetFcpPersistentBinding_IN structure is used to pass input parameter data to the GetFcpPersistentBinding WMI method
old-location: storage\getfcppersistentbinding_in.htm
tech.root: storage
ms.date: 03/29/2018
keywords: ["GetFcpPersistentBinding_IN structure"]
ms.keywords: "*PGetFcpPersistentBinding_IN, GetFcpPersistentBinding_IN, GetFcpPersistentBinding_IN structure [Storage Devices], PGetFcpPersistentBinding_IN, PGetFcpPersistentBinding_IN structure pointer [Storage Devices], _GetFcpPersistentBinding_IN, hbapiwmi/GetFcpPersistentBinding_IN, hbapiwmi/PGetFcpPersistentBinding_IN, storage.getfcppersistentbinding_in, structs-Fibre_34b0e554-331b-4f99-ae8e-5c2e9855b641.xml"
req.header: hbapiwmi.h
req.include-header: Hbapiwmi.h
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
req.typenames: GetFcpPersistentBinding_IN, *PGetFcpPersistentBinding_IN
f1_keywords:
 - _GetFcpPersistentBinding_IN
 - hbapiwmi/_GetFcpPersistentBinding_IN
 - PGetFcpPersistentBinding_IN
 - hbapiwmi/PGetFcpPersistentBinding_IN
 - GetFcpPersistentBinding_IN
 - hbapiwmi/GetFcpPersistentBinding_IN
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - hbapiwmi.h
api_name:
 - GetFcpPersistentBinding_IN
---

# _GetFcpPersistentBinding_IN structure


## -description

The GetFcpPersistentBinding_IN structure is used to pass input parameter data to the <a href="/windows-hardware/drivers/storage/getfcppersistentbinding">GetFcpPersistentBinding</a> WMI method

## -struct-fields

### -field InEntryCount

Indicates the number of binding entries that will fit in the buffer that the WMI client provides when it calls the <a href="/windows-hardware/drivers/storage/getfcppersistentbinding">GetFcpPersistentBinding</a> WMI method.

## -remarks

The WMI tool suite generates a declaration of the GetFcpPersistentBinding_IN structure in <i>Hbapiwmi.h </i>when it compiles the <a href="/windows-hardware/drivers/storage/msfc-hbafcpinfo-wmi-class">MSFC_HBAFCPInfo WMI Class</a>.

## -see-also

<a href="/windows-hardware/drivers/storage/getfcppersistentbinding">GetFcpPersistentBinding</a>



<a href="/windows-hardware/drivers/storage/msfc-hbafcpinfo-wmi-class">MSFC_HBAFCPInfo WMI Class</a>
