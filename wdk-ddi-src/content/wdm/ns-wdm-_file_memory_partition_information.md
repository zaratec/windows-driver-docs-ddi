---
UID: NS:wdm._FILE_MEMORY_PARTITION_INFORMATION
title: _FILE_MEMORY_PARTITION_INFORMATION (wdm.h)
description: Stores information about memory partition. This structure is used by the ZwSetInformationFile function.
old-location: ifsk\_file_memory_partition_information.htm
tech.root: ifsk
ms.date: 04/16/2018
keywords: ["FILE_MEMORY_PARTITION_INFORMATION structure"]
ms.keywords: "*PFILE_MEMORY_PARTITION_INFORMATION, FILE_MEMORY_PARTITION_INFORMATION, FILE_MEMORY_PARTITION_INFORMATION structure [Kernel-Mode Driver Architecture], _FILE_MEMORY_PARTITION_INFORMATION, ifsk._file_memory_partition_information, wdm/FILE_MEMORY_PARTITION_INFORMATION"
req.header: wdm.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1709
req.target-min-winversvr: Windows Server 2016
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
req.typenames: FILE_MEMORY_PARTITION_INFORMATION, *PFILE_MEMORY_PARTITION_INFORMATION
f1_keywords:
 - _FILE_MEMORY_PARTITION_INFORMATION
 - wdm/_FILE_MEMORY_PARTITION_INFORMATION
 - PFILE_MEMORY_PARTITION_INFORMATION
 - wdm/PFILE_MEMORY_PARTITION_INFORMATION
 - FILE_MEMORY_PARTITION_INFORMATION
 - wdm/FILE_MEMORY_PARTITION_INFORMATION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wdm.h
api_name:
 - FILE_MEMORY_PARTITION_INFORMATION
---

# _FILE_MEMORY_PARTITION_INFORMATION structure


## -description

<p class="CCE_Message">[Some information relates to pre-released product which may be substantially modified before it's commercially released. Microsoft makes no warranties, express or implied, with respect to the information provided here.]

Stores information about memory partition. This structure is used by the <b>ZwSetInformationFile</b> function.

## -struct-fields

### -field OwnerPartitionHandle

Handle to the specified partition.

### -field Flags

### -field Flags.DUMMYSTRUCTNAME

### -field Flags.DUMMYSTRUCTNAME.NoCrossPartitionAccess

Determines whether cross-partition access is allowed.

### -field Flags.DUMMYSTRUCTNAME.Spare

### -field Flags.AllFlags

Bitwise of all flags.

