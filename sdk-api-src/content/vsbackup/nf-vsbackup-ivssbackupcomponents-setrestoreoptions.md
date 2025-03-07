---
UID: NF:vsbackup.IVssBackupComponents.SetRestoreOptions
title: IVssBackupComponents::SetRestoreOptions (vsbackup.h)
description: The SetRestoreOptions method sets a string of private, or writer-dependent, restore parameters for a writer component.
helpviewer_keywords: ["IVssBackupComponents interface [VSS]","SetRestoreOptions method","IVssBackupComponents.SetRestoreOptions","IVssBackupComponents::SetRestoreOptions","SetRestoreOptions","SetRestoreOptions method [VSS]","SetRestoreOptions method [VSS]","IVssBackupComponents interface","_win32_ivssbackupcomponents_setrestoreoptions","base.ivssbackupcomponents_setrestoreoptions","vsbackup/IVssBackupComponents::SetRestoreOptions"]
old-location: base\ivssbackupcomponents_setrestoreoptions.htm
tech.root: base
ms.assetid: 4a872594-dcd8-463d-9f6b-6bc40c17df38
ms.date: 12/05/2018
ms.keywords: IVssBackupComponents interface [VSS],SetRestoreOptions method, IVssBackupComponents.SetRestoreOptions, IVssBackupComponents::SetRestoreOptions, SetRestoreOptions, SetRestoreOptions method [VSS], SetRestoreOptions method [VSS],IVssBackupComponents interface, _win32_ivssbackupcomponents_setrestoreoptions, base.ivssbackupcomponents_setrestoreoptions, vsbackup/IVssBackupComponents::SetRestoreOptions
f1_keywords:
- vsbackup/IVssBackupComponents.SetRestoreOptions
dev_langs:
- c++
req.header: vsbackup.h
req.include-header: VsBackup.h, Vss.h, VsWriter.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: VssApi.lib
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- VssApi.lib
- VssApi.dll
api_name:
- IVssBackupComponents.SetRestoreOptions
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IVssBackupComponents::SetRestoreOptions


## -description


The <b>SetRestoreOptions</b> method 
    sets a string of private, or writer-dependent, restore parameters for a writer component.


## -parameters




### -param writerId [in]

Writer identifier.


### -param ct [in]

Type of the component. See <a href="https://docs.microsoft.com/windows/desktop/api/vswriter/ne-vswriter-vss_component_type">VSS_COMPONENT_TYPE</a> 
      for the possible values.


### -param wszLogicalPath [in]

Null-terminated wide character string containing the logical path of the component. 
      For more information, see <a href="https://docs.microsoft.com/windows/desktop/VSS/logical-pathing-of-components">Logical Pathing of Components</a>.

The value of the string containing the logical path used here should be the same as was used when the 
       component was added to the backup set using 
       <a href="https://docs.microsoft.com/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-addcomponent">IVssBackupComponents::AddComponent</a>.

The logical path can be <b>NULL</b>.

There are no restrictions on the characters that can appear in a non-NULL logical path.


### -param wszComponentName [in]

Null-terminated wide character string containing the name of the component. 
      

The string cannot be <b>NULL</b> and should contain the same component name as was used when the component was added 
      to the backup set using 
      <a href="https://docs.microsoft.com/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-addcomponent">IVssBackupComponents::AddComponent</a>.


### -param wszRestoreOptions [in]

Null-terminated wide character string containing the private string of restore parameters. For more 
      information see <a href="https://docs.microsoft.com/windows/desktop/VSS/setting-vss-restore-options">Setting VSS Restore 
      Options</a>.


## -returns



The following are the valid return codes for this method.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Successfully set the previous backup time stamp.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One of the parameter values is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
The caller is out of memory or other system resources.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VSS_E_BAD_STATE</b></dt>
</dl>
</td>
<td width="60%">
The backup components object is not initialized, this method has been called during a restore operation, 
        or this method has not been called within the correct sequence.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VSS_E_OBJECT_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The backup component does not exist.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VSS_E_INVALID_XML_DOCUMENT</b></dt>
</dl>
</td>
<td width="60%">
The XML document is not valid. Check the event log for details. For more 
        information, see 
        <a href="https://docs.microsoft.com/windows/desktop/VSS/event-and-error-handling-under-vss">Event and Error Handling Under VSS</a>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VSS_E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
Unexpected error. The error code is logged in the error log file. For more information, see 
        <a href="https://docs.microsoft.com/windows/desktop/VSS/event-and-error-handling-under-vss">Event and Error Handling Under VSS</a>.

<b>Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>This value is not supported until Windows Server 2008 R2 and Windows 7. E_UNEXPECTED is used instead.

</td>
</tr>
</table>
 




## -remarks



This method must be called before 
    <a href="https://docs.microsoft.com/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-prerestore">IVssBackupComponents::PreRestore</a>.

The exact syntax and content of the restore options set by the <i>wszRestoreOptions</i> 
    parameter of the 
    <b>SetRestoreOptions</b> method will 
    depend on the specific writer being contacted.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/vsbackup/nl-vsbackup-ivssbackupcomponents">IVssBackupComponents</a>



<a href="https://docs.microsoft.com/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-prerestore">IVssBackupComponents::PreRestore</a>



<a href="https://docs.microsoft.com/windows/desktop/api/vswriter/ne-vswriter-vss_component_type">VSS_COMPONENT_TYPE</a>
 

 

