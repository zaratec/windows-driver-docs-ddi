---
UID: NF:scavengr.RxScavengeFobxsForNetRoot
title: RxScavengeFobxsForNetRoot function (scavengr.h)
description: RxScavengeFobxsForNetRoot scavenges all of the FOBX structures associated with a given NET_ROOT structure.
old-location: ifsk\rxscavengefobxsfornetroot.htm
tech.root: ifsk
ms.date: 04/16/2018
keywords: ["RxScavengeFobxsForNetRoot function"]
ms.keywords: RxScavengeFobxsForNetRoot, RxScavengeFobxsForNetRoot function [Installable File System Drivers], ifsk.rxscavengefobxsfornetroot, rxref_9fac9a87-f068-4ee4-909c-85a41c9884d6.xml, scavengr/RxScavengeFobxsForNetRoot
req.header: scavengr.h
req.include-header: Rxprocs.h
req.target-type: Desktop
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
req.irql: <= APC_LEVEL
targetos: Windows
req.typenames: 
f1_keywords:
 - RxScavengeFobxsForNetRoot
 - scavengr/RxScavengeFobxsForNetRoot
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - scavengr.h
api_name:
 - RxScavengeFobxsForNetRoot
---

# RxScavengeFobxsForNetRoot function


## -description

<b>RxScavengeFobxsForNetRoot</b> scavenges all of the FOBX structures associated with a given NET_ROOT structure.

## -parameters

### -param NetRoot

A pointer to the NET_ROOT structure for which the FOBX structures need to be scavenged.

### -param PurgingFcb

A pointer to the FCB for which the scavenging should occur.

### -param SynchronizeWithScavenger

A Boolean value that specifies if this routine should synchronize with the scavenger.

## -remarks

At cleanup, there are no more user handles associated with the file object. In such cases, the time window between close and cleanup is dictated by the additional references maintained by the memory manager and cache manager. On cleanup, the FOBX is put on a close pending list and removed from the corresponding list when a close operation is received. In the interim, if an open operation is failing with ACCESS_DENIED status, then RDBSS can force a purge and scavenge of the FOBX structure. This is a synchronous operation.

For directory renames, all files under the directory need to be closed. So, a network mini-redirector might call <b>RxPurgeRelatedFobxs</b> and <b>RxScavengeFobxsForNetRoot</b> in response to a IRP_MJ_SET_INFORMATION request to rename a directory. By passing in the NET_ROOT structure for the directory and a <b>NULL</b> FCB, all of the FOBX structures associated with the directory would be purged and scavenged.

The <b>RxScavengeFobxsForNetRoot</b> routine acquires the scavenger mutex, traverses the <b>FobxsToBeFinalized</b> list member of the scavenger object and adds any entries found to tail of the <b>ScavengerFinalizationList</b> member of the scavenger object, and then releases the mutex. 

If <i>PurgingFcb </i>is not <b>NULL</b>, and this purging FCB structure is not the same as the FCB associated with the FOBX structure on the <b>FobxsToBeFinalized</b> list member of the scavenger object, <b>RxScavengeFobxsForNetRoot</b> will call the <a href="/windows-hardware/drivers/ddi/mrx/nc-mrx-pmrx_chkfcb_calldown">MRxAreFilesAliased</a> callback routine provided by the network mini-redirector if it is supported. The call to <b>MRxAreFilesAliased</b> is to determine if the PFCB is an alias for the FCB associated with the FOBX structure.

On checked builds, <b>RxScavengeAllFobxs</b> causes the system to ASSERT for the following condition:

<ul>
<li>
The <b>NodeTypeCode</b> member of an FOBX structure is not RDBSS_NTC_FOBX.

</li>
</ul>

## -see-also

<a href="/windows-hardware/drivers/ddi/mrx/nc-mrx-pmrx_chkfcb_calldown">MRxAreFilesAliased</a>



<a href="/windows-hardware/drivers/ddi/rxprocs/nf-rxprocs-rxpurgeallfobxs">RxPurgeAllFobxs</a>



<a href="/windows-hardware/drivers/ddi/scavengr/nf-scavengr-rxpurgerelatedfobxs">RxPurgeRelatedFobxs</a>



<a href="/windows-hardware/drivers/ddi/rxprocs/nf-rxprocs-rxscavengeallfobxs">RxScavengeAllFobxs</a>
