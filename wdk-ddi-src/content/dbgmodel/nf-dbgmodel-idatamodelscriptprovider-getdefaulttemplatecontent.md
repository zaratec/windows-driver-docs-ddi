---
UID: NF:dbgmodel.IDataModelScriptProvider.GetDefaultTemplateContent
title: IDataModelScriptProvider::GetDefaultTemplateContent (dbgmodel.h)
description: The GetDefaultTemplateContent method returns an interface for the default template content of the provider.
ms.date: 08/20/2018
keywords: ["IDataModelScriptProvider::GetDefaultTemplateContent"]
ms.keywords: IDataModelScriptProvider::GetDefaultTemplateContent, GetDefaultTemplateContent, IDataModelScriptProvider.GetDefaultTemplateContent, IDataModelScriptProvider::GetDefaultTemplateContent, IDataModelScriptProvider.GetDefaultTemplateContent
req.header: dbgmodel.h
req.include-header: 
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.lib: 
req.dll: 
req.irql: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
targetos: Windows
tech.root: debugger
ms.custom: RS5
f1_keywords:
 - IDataModelScriptProvider::GetDefaultTemplateContent
 - dbgmodel/IDataModelScriptProvider::GetDefaultTemplateContent
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - dbgmodel.h
api_name:
 - IDataModelScriptProvider.GetDefaultTemplateContent
---

# IDataModelScriptProvider::GetDefaultTemplateContent


## -description

The GetDefaultTemplateContent method returns an interface for the default template content of the provider. This is content that the script provider would like pre-populated in an edit window for a newly created script. If the script provider has no templates (or has no template content which is designated as the default content), the script provider may return E_NOTIMPL from this method.

## -parameters

### -param templateContent

The default template content for the script provider is returned here as a component implementing the [IDataModelScriptTemplate](nn-dbgmodel-idatamodelscripttemplate.md) interface.

## -returns

This method returns HRESULT that indicates success or failure.

## -remarks

## -see-also

[IDataModelScriptProvider interface](nn-dbgmodel-idatamodelscriptprovider.md)

