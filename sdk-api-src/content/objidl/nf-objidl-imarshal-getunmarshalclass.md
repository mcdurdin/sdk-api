---
UID: NF:objidl.IMarshal.GetUnmarshalClass
title: IMarshal::GetUnmarshalClass (objidl.h)
description: Retrieves the CLSID of the unmarshaling code.
helpviewer_keywords: ["GetUnmarshalClass","GetUnmarshalClass method [COM]","GetUnmarshalClass method [COM]","IMarshal interface","IMarshal interface [COM]","GetUnmarshalClass method","IMarshal.GetUnmarshalClass","IMarshal::GetUnmarshalClass","_com_imarshal_getunmarshalclass","com.imarshal_getunmarshalclass","objidl/IMarshal::GetUnmarshalClass"]
old-location: com\imarshal_getunmarshalclass.htm
tech.root: com
ms.assetid: 900a0f19-dcd5-4135-bab8-c191ec7e95e4
ms.date: 12/05/2018
ms.keywords: GetUnmarshalClass, GetUnmarshalClass method [COM], GetUnmarshalClass method [COM],IMarshal interface, IMarshal interface [COM],GetUnmarshalClass method, IMarshal.GetUnmarshalClass, IMarshal::GetUnmarshalClass, _com_imarshal_getunmarshalclass, com.imarshal_getunmarshalclass, objidl/IMarshal::GetUnmarshalClass
f1_keywords:
- objidl/IMarshal.GetUnmarshalClass
dev_langs:
- c++
req.header: objidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: ObjIdl.idl
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
- COM
api_location:
- ObjIdl.h
api_name:
- IMarshal.GetUnmarshalClass
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMarshal::GetUnmarshalClass


## -description


Retrieves the CLSID of the unmarshaling code.


## -parameters




### -param riid [in]

A reference to the identifier of the interface to be marshaled.


### -param pv [in]

A pointer to the interface to be marshaled; can be <b>NULL</b> if the caller does not have a pointer to the desired interface.


### -param dwDestContext [in]

The destination context where the specified interface is to be unmarshaled. Possible values come from the enumeration <a href="https://docs.microsoft.com/windows/desktop/api/wtypesbase/ne-wtypesbase-mshctx">MSHCTX</a>. Unmarshaling can occur either in another apartment of the current process (MSHCTX_INPROC) or in another process on the same computer as the current process (MSHCTX_LOCAL).


### -param pvDestContext [in]

This parameter is reserved and must be <b>NULL</b>.


### -param mshlflags [in]

Indicates whether the data to be marshaled is to be transmitted back to the client processâ€”the typical caseâ€”or written to a global table, where it can be retrieved by multiple clients. Possible values come from the <a href="https://docs.microsoft.com/windows/desktop/api/wtypesbase/ne-wtypesbase-mshlflags">MSHLFLAGS</a> enumeration.


### -param pCid [out]

A pointer that receives the CLSID to be used to create a proxy in the client process.


## -returns



If the method succeeds, the return value is S_OK. Otherwise, it is S_FALSE.




## -remarks



This method is called indirectly, in  a call to <a href="https://docs.microsoft.com/windows/desktop/api/combaseapi/nf-combaseapi-comarshalinterface">CoMarshalInterface</a>, by whatever code in the server process is responsible for marshaling a pointer to an interface on an object. This marshaling code is usually a stub generated by COM for one of several interfaces that can marshal a pointer to an interface implemented on an entirely different object. Examples include the <a href="https://docs.microsoft.com/windows/desktop/api/unknwnbase/nn-unknwnbase-iclassfactory">IClassFactory</a> and <a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nn-oleidl-ioleitemcontainer">IOleItemContainer</a> interfaces. For purposes of discussion, the code responsible for marshaling a pointer is called the <i>marshaling stub</i>.

To create a proxy for an object, COM requires two pieces of information from the original object: the amount of data to be written to the marshaling stream and the proxy's CLSID.

The marshaling stub obtains these two pieces of information with successive calls to <a href="https://docs.microsoft.com/windows/desktop/api/combaseapi/nf-combaseapi-cogetmarshalsizemax">CoGetMarshalSizeMax</a> and <a href="https://docs.microsoft.com/windows/desktop/api/combaseapi/nf-combaseapi-comarshalinterface">CoMarshalInterface</a>.

<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
The marshaling stub calls the object's implementation of this method to obtain the CLSID to be used in creating an instance of the proxy. The client, upon receiving the CLSID, loads the DLL listed for it in the system registry.

You do not explicitly call this method if you are implementing existing COM interfaces or using the Microsoft Interface Definition Language (MIDL) to define your own interfaces. In either case, the stub automatically makes the call. See <a href="https://docs.microsoft.com/windows/desktop/com/defining-com-interfaces">Defining COM Interfaces</a>.

If you are not using MIDL to define your own interface, your stub must call this method, either directly or indirectly, to get the CLSID that the client-side COM library needs to create a proxy for the object implementing the interface.

If the caller has a pointer to the interface to be marshaled, it should, as a matter of efficiency, use the <i>pv</i> parameter to pass that pointer. In this way, an implementation that may use such a pointer to determine the appropriate CLSID for the proxy does not have to call <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> on itself. If a caller does not have a pointer to the interface to be marshaled, it can pass <b>NULL</b>.

<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
COM calls <b>GetUnmarshalClass</b> to obtain the CLSID to be used for creating a proxy in the client process. The CLSID to be used for a proxy is normally not that of the original object, but one you will have generated (using the Guidgen.exe tool) specifically for your proxy object.

Implement this method for each object that provides marshaling for one or more of its interfaces. The code responsible for marshaling the object writes the CLSID, along with the marshaling data, to a stream; COM extracts the CLSID and data from the stream on the receiving side.

If your proxy implementation consists simply of copying the entire original object into the client process, thereby eliminating the need to forward calls to the original object, the CLSID returned would be the same as that of the original object. This strategy, of course, is advisable only for objects that are not expected to change.

If the <i>pv</i> parameter is <b>NULL</b> and your implementation needs an interface pointer, it can call <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> on the current object to get it. The <i>pv</i> parameter exists merely to improve efficiency.

To ensure that your implementation of <b>GetUnmarshalClass</b> continues to work properly as new destination contexts are supported in the future, delegate marshaling to the COM default implementation for all <i>dwDestContext</i> values that your implementation does not handle. To delegate marshaling to the COM default implementation, call the <a href="https://docs.microsoft.com/windows/desktop/api/combaseapi/nf-combaseapi-cogetstandardmarshal">CoGetStandardMarshal</a> function.


<div class="alert"><b>Note</b>  The <b>ThreadingModel</b> registry value must be <b>Both</b> for an in-process server that implements the CLSID returned from the <b>GetUnmarshalClass</b> method.
For more information, see <a href="https://docs.microsoft.com/windows/desktop/com/inprocserver32">InprocServer32</a>.</div>
<div> </div>





## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/combaseapi/nf-combaseapi-comarshalinterface">CoMarshalInterface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-imarshal">IMarshal</a>
 

 

