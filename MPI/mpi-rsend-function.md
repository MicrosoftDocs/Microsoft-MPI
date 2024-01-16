---
title: MPI_Rsend function
TOCTitle: MPI_Rsend function
ms:assetid: 28076c76-7ea3-4ac3-996c-b36619565227
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473462(v=VS.85)
ms:contentKeyID: 59360997
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_RSEND
- mpif/MPI_Rsend
- mpi/MPI_RSEND
dev_langs:
- C++
- C
api_location:
- Msmpi.dll
api_name:
- MPI_Rsend
api_type:
- DLLExport
product:
- Windows
topic_type:
- apiref
- kbSyntax
product_family_name: VS
ROBOTS: INDEX,FOLLOW
description: Learn about the MPI_Rsend function on Microsoft's official site. Understand its syntax, parameters, return value, and how it improves performance in data sending operations.
---

# MPI\_Rsend function

Performs a ready mode send operation and returns when the send buffer can be safely reused.

## Syntax

``` c++
int MPIAPI MPI_Rsend(
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

``` FORTRAN
    MPI_RSEND(BUF, COUNT, DATATYPE, DEST, TAG, COMM, IERROR)
        <type> BUF(*)
        INTEGER COUNT, DATATYPE, DEST, TAG, COMM, IERROR
```

## Remarks

This function is non-local. This function returns as soon as the send buffer can be reused and does not depend on the status of a matching receive operation. However, the successful completion of the overall send operation depends on the existence of a matching receive operation.

This function can only be called if the matching receive operation is already posted. Otherwise, the function returns an error and its result is undefined. On some systems, this requirement eliminates some of the handshaking that is used in other modes, and can improve performance compared to the standard or synchronous send operations.

The **MPI\_Rsend** function has the same semantics as the [**MPI\_Send**](mpi-send-function.md) and [**MPI\_Ssend**](mpi-ssend-function.md) functions, but it notifies the system that a matching receive is already posted. That information can save some overhead. Therefore, in a correct program, a ready send could be replaced by a standard send with no effect on the behavior of the program other than performance.

## Requirements

<table>
<colgroup>
<col/>
<col/>
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

[**MPI\_Send**](mpi-send-function.md)

[**MPI\_Bsend**](mpi-bsend-function.md)

[**MPI\_Ssend**](mpi-ssend-function.md)

[**MPI\_Recv**](mpi-recv-function.md)

