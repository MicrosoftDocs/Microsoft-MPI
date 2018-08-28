---
title: MPI_Send function
TOCTitle: MPI_Send function
ms:assetid: 02e5b56e-a813-46bc-8927-b9481b932830
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473467(v=VS.85)
ms:contentKeyID: 59361002
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_SEND
- mpif/MPI_Send
- mpi/MPI_SEND
dev_langs:
- C++
- C
api_location:
- Msmpi.dll
api_name:
- MPI_Send
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

# MPI\_Send function

Performs a standard mode send operation and returns when the send buffer can be safely reused.

## Syntax

``` c++
int MPIAPI MPI_Send(
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
    The number of elements in the buffer. If the data part of the message is empty, set the *count* parameter to 0.

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

    MPI_SEND(BUF, COUNT, DATATYPE, DEST, TAG, COMM, IERROR)
        <type> BUF(*)
        INTEGER COUNT, DATATYPE, DEST, TAG, COMM, IERROR

## Remarks

This function is non-local. Successful completion might depend on the existence of a matching receive function.

This function can return before a matching receive function is invoked if the MPI implementation buffers the message. However, buffer space might be unavailable, or outgoing messages might not be buffered for performance reasons. If the message is not buffered, the function does not return until the data has been moved to the receiving process.

This function can be called whether or not a matching receive function is posted. It might finish before a matching receive function is posted.

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

[**MPI\_Bsend**](mpi-bsend-function.md)

[**MPI\_Rsend**](mpi-rsend-function.md)

[**MPI\_Ssend**](mpi-ssend-function.md)

[**MPI\_Recv**](mpi-recv-function.md)

