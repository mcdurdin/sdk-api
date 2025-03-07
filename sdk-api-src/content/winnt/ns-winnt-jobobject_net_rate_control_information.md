---
UID: NS:winnt.JOBOBJECT_NET_RATE_CONTROL_INFORMATION
title: JOBOBJECT_NET_RATE_CONTROL_INFORMATION (winnt.h)
description: Contains information used to control the network traffic for a job. This structure is used by the SetInformationJobObject and QueryInformationJobObject functions with the JobObjectNetRateControlInformation information class.
helpviewer_keywords: ["JOBOBJECT_NET_RATE_CONTROL_INFORMATION","JOBOBJECT_NET_RATE_CONTROL_INFORMATION structure","base.jobobject_net_rate_control_information","winnt/JOBOBJECT_NET_RATE_CONTROL_INFORMATION"]
old-location: base\jobobject_net_rate_control_information.htm
tech.root: backup
ms.assetid: CE55BC2A-B27C-490A-9D5A-C18FEC09638C
ms.date: 12/05/2018
ms.keywords: JOBOBJECT_NET_RATE_CONTROL_INFORMATION, JOBOBJECT_NET_RATE_CONTROL_INFORMATION structure, base.jobobject_net_rate_control_information, winnt/JOBOBJECT_NET_RATE_CONTROL_INFORMATION
f1_keywords:
- winnt/JOBOBJECT_NET_RATE_CONTROL_INFORMATION
dev_langs:
- c++
req.header: winnt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
- Winnt.h
api_name:
- JOBOBJECT_NET_RATE_CONTROL_INFORMATION
targetos: Windows
req.typenames: JOBOBJECT_NET_RATE_CONTROL_INFORMATION
req.redist: 
ms.custom: 19H1
---

# JOBOBJECT_NET_RATE_CONTROL_INFORMATION structure


## -description


Contains information used to control the network traffic for a job. This structure is used by the <a href="https://docs.microsoft.com/windows/desktop/api/jobapi2/nf-jobapi2-setinformationjobobject">SetInformationJobObject</a> and <a href="https://docs.microsoft.com/windows/desktop/api/jobapi2/nf-jobapi2-queryinformationjobobject">QueryInformationJobObject</a> functions with the <b>JobObjectNetRateControlInformation</b> information class.


## -struct-fields




### -field MaxBandwidth

The maximum bandwidth for outgoing network traffic for the job, in bytes.


### -field ControlFlags

A combination of <a href="https://docs.microsoft.com/windows/desktop/api/winnt/ne-winnt-job_object_net_rate_control_flags">JOB_OBJECT_NET_RATE_CONTROL_FLAGS</a> enumeration values that specify the scheduling policy for network rate control.


### -field DscpTag

The value to use for the Differentiated Service code point (DSCP) field to turn on network quality of service (QoS) for all outgoing network traffic generated by the processes of the job object. The valid range is from 0x00 through 0x3F. For information about DSCP, see <a href="https://docs.microsoft.com/previous-versions/windows/desktop/qos/differentiated-services">Differentiated Services</a>.


## -remarks



You can only set the control of the network traffic on one job in a hierarchy of nested jobs. The settings that you specify apply to that job and the child jobs in the hierarchy for that job.  The settings do not apply to the chain of jobs from the parent job up to the top of the hierarchy. You can change the settings on the original job in the hierarchy on which you set rate control. However, attempts to set values for the control of the network rate for any other jobs in the hierarchy, including the parent jobs, fail.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/winnt/ne-winnt-job_object_net_rate_control_flags">JOB_OBJECT_NET_RATE_CONTROL_FLAGS</a>



<a href="https://docs.microsoft.com/windows/desktop/api/jobapi2/nf-jobapi2-queryinformationjobobject">QueryInformationJobObject</a>



<a href="https://docs.microsoft.com/windows/desktop/api/jobapi2/nf-jobapi2-setinformationjobobject">SetInformationJobObject</a>
 

 

