---
title: MPI_Bsend function
TOCTitle: MPI_Bsend function
ms:assetid: 991fa16c-06bd-4aff-9a04-35ba13c4ea69
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473238(v=VS.85)
ms:contentKeyID: 59360784
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_BSEND
- mpif/MPI_Bsend
- mpi/MPI_BSEND
dev_langs:
- C++
- C
api_location:
- Msmpi.dll
api_name:
- MPI_Bsend
api_type:
- DLLExport
product:
- Windows
topic_type:
- apiref
- kbSyntax
product_family_name: VS
ROBOTS: INDEX,FOLLOW
---

# MPI\_Bsend function

Sends data to a specified process in buffered mode. This function returns when the send buffer can be safely reused.

## Syntax

``` c++
int MPIAPI MPI_Bsend(
  _In_opt_ void         *buf,
           int          count,
           MPI_Datatype datatype,
           int          dest,
           int          tag,
           MPI_Comm     comm
);
```

## Parameters

  - *buf* \[in, optional\]  
    A pointer to the buffer that contains the data to be sent.

  - *count*  
    The number of elements in the buffer array. If the data part of the message is empty, set the *count* parameter to 0.

  - *datatype*  
    The data type of the elements in the buffer.

  - *dest*  
    The rank of the destination process within the communicator that is specified by the *comm* parameter.

  - *tag*  
    The message tag that can be used to distinguish different types of messages.

  - *comm*  
    The handle to the communicator.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

    MPI_BSEND(BUF, COUNT, DATATYPE, DEST, TAG, COMM, IERROR)
        <type> BUF(*)
        INTEGER COUNT, DATATYPE, DEST, TAG, COMM, IERROR

## Remarks

This function is local, it can complete the send operation successfully without the occurrence of a matching receive operation.

This function can be started whether or not a matching receive operation has been posted. It can complete the send operation before a matching receive is posted. Its completion does not depend on the occurrence of a matching receive operation. If you call this function and no matching receive operation is posted, the MPI implementation must buffer the outgoing message so that the send call can return.

This function returns an error if there is insufficient buffer space. The amount of available buffer space is controlled by the user by using the [**MPI\_Buffer\_attach**](mpi-buffer-attach-function.md) function.

## Requirements

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Product</p></td>
<td><p>HPC Pack 2012 MS-MPI Redistributable Package, HPC Pack 2008 R2 MS-MPI Redistributable Package, HPC Pack 2008 MS-MPI Redistributable Package or HPC Pack 2008 Client Utilities</p></td>
</tr>
<tr class="even">
<td><p>Header</p></td>
<td>Mpi.h;
Mpif.h</td>
</tr>
<tr class="odd">
<td><p>Library</p></td>
<td>Msmpi.lib</td>
</tr>
<tr class="even">
<td><p>DLL</p></td>
<td>Msmpi.dll</td>
</tr>
</tbody>
</table>


## See also

[MPI Point to Point Functions](mpi-point-to-point-functions.md)

[**MPI\_Buffer\_attach**](mpi-buffer-attach-function.md)

[**MPI\_Send**](mpi-send-function.md)

[**MPI\_Ssend**](mpi-ssend-function.md)

[**MPI\_Rsend**](mpi-rsend-function.md)

[**MPI\_Recv**](mpi-recv-function.md)

