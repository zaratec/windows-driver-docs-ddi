---
UID: NF:sensorsclassextension.ISensorClassExtension.Uninitialize
title: ISensorClassExtension::Uninitialize (sensorsclassextension.h)
description: The ISensorClassExtension::Uninitialize method uninitializes the sensor class extension object.
old-location: sensors\isensorclassextension_uninitialize.htm
tech.root: sensors
ms.date: 05/03/2018
keywords: ["ISensorClassExtension::Uninitialize"]
ms.keywords: ISensorClassExtension interface [Sensor Devices],Uninitialize method, ISensorClassExtension.Uninitialize, ISensorClassExtension::Uninitialize, Uninitialize, Uninitialize method [Sensor Devices], Uninitialize method [Sensor Devices],ISensorClassExtension interface, sensors.isensorclassextension_uninitialize, sensorsclassextension/ISensorClassExtension::Uninitialize
req.header: sensorsclassextension.h
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
req.lib: SensorsClassExtension.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
f1_keywords:
 - ISensorClassExtension::Uninitialize
 - sensorsclassextension/ISensorClassExtension::Uninitialize
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - SensorsClassExtension.lib
 - SensorsClassExtension.dll
api_name:
 - Uninitialize
---

# ISensorClassExtension::Uninitialize


## -description

The <a href="/windows-hardware/drivers/ddi/sensorsclassextension/nf-sensorsclassextension-isensorclassextension-uninitialize">ISensorClassExtension::Uninitialize</a> method uninitializes the sensor class extension object.

## -returns

This method returns an HRESULT. Possible values include, but are not limited to, one of the following values.

|Return code|Description|
|--- |--- |
|S_OK|The method succeeded.|
|HRESULT_FROM_WIN32(ERROR_CAN_NOT_COMPLETE)|The class extension is not initialized.|

## -remarks

Typically, you will uninitialize  the sensor class extension when the driver is unloading. We recommend that you perform uninitialization steps when called by UMDF in <a href="/windows-hardware/drivers/ddi/wudfddi/nf-wudfddi-ipnpcallbackhardware-onreleasehardware">IPnpCallbackHardware::OnReleaseHardware</a>.

If you must, for some reason, otherwise release and uninitialize the sensor class extension, you must call <a href="/windows-hardware/drivers/ddi/wudfddi/nf-wudfddi-iwdfioqueue-drainsynchronously">IWDFIoQueue::DrainSynchronously</a> before calling <a href="/windows-hardware/drivers/ddi/sensorsclassextension/nf-sensorsclassextension-isensorclassextension-uninitialize">ISensorClassExtension::Uninitialize</a>. You can retrieve the queue interface by calling <a href="/windows-hardware/drivers/ddi/wudfddi/nf-wudfddi-iwdfdevice-getdefaultioqueue">IWDFDevice::GetDefaultIoQueue</a> on the WDF device object. Then, call <b>IWDFIoQueue::DrainSynchronously</b> to process all the queued requests. Calling <b>IWDFIoQueue::DrainSynchronously</b> blocks the queuing of new requests, so you must call <a href="/windows-hardware/drivers/ddi/wudfddi/nf-wudfddi-iwdfioqueue-start">IWDFIoQueue::Start</a> after you reinitialize the class extension.

## -see-also

<a href="/windows-hardware/drivers/ddi/sensorsclassextension/nn-sensorsclassextension-isensorclassextension">ISensorClassExtension</a>
