---
title: MPI_Ssend function
TOCTitle: MPI_Ssend function
ms:assetid: dea32116-1bf7-479a-a5c0-25158844a739
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473471(v=VS.85)
ms:contentKeyID: 59361006
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_SSEND
- mpif/MPI_Ssend
- mpi/MPI_SSEND
dev_langs:
- C++
- C
api_location:
- Msmpi.dll
api_name:
- MPI_Ssend
api_type:
- DLLExport
product:
- Windows
topic_type:
- apiref
- kbSyntax
product_family_name: VS
ROBOTS: INDEX,FOLLOW
description: Master Microsoft's Message Passing Interface (MPI) with the MPI_Ssend function for synchronous mode send operations. Learn more now.
---

# MPI\_Ssend function

Performs a synchronous mode send operation and returns when the send buffer can be safely reused.

## Syntax

``` c++
int MPIAPI MPI_Ssend(
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
    MPI_SSEND(BUF, COUNT, DATATYPE, DEST, TAG, COMM, IERROR)
        <type> BUF(*)
        INTEGER COUNT, DATATYPE, DEST, TAG, COMM, IERROR
```

## Remarks

This function is non-local. Successful completion of the send operation depends on the occurrence of a matching receive function.

This function can be called whether or not a matching receive is posted. However, the send function is completed successfully only if a matching receive is posted, and the receive operation has started to receive the message. Therefore, the completion of a synchronous send not only indicates that the send buffer can be reused, but it also indicates that the receiving process has started to execute the matching receive.

If both send and receive operations are blocking operations, then the synchronous mode provides synchronous communication semantics; a communication is not completed at either end until the send and receive processes have finished.

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

[**MPI\_Rsend**](mpi-rsend-function.md)

[**MPI\_Recv**](mpi-recv-function.md)

