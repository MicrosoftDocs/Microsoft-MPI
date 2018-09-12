---
title: MPI_Irsend function
TOCTitle: MPI_Irsend function
ms:assetid: be8e193d-4341-4f20-aa31-40c9640a8bca
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473426(v=VS.85)
ms:contentKeyID: 59360962
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_IRSEND
- mpif/MPI_Irsend
- mpi/MPI_IRSEND
dev_langs:
- C++
- C
api_location:
- Msmpi.dll
api_name:
- MPI_Irsend
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

# MPI\_Irsend function

Initiates a ready mode send operation and returns a request handle that represents the communication operation.

## Syntax

``` c++
int MPIAPI MPI_Irsend(
  _In_opt_ void         *buf,
           int          count,
           MPI_Datatype datatype,
           int          dest,
           int          tag,
           MPI_Comm     comm,
  _Out_    MPI_Request  *request
);
```

## Parameters

  - *buf* \[in, optional\]  
    A pointer to the buffer that contains the data to be sent. The buffer consists of count successive elements of the MPI\_Datatype object that is indicated by the *datatype* handle. The message length is specified in terms of number of elements, not in number of bytes. The caller should not modify any part of the send buffer until the communication operation is completed.

  - *count*  
    The number of elements in the buffer array. If count is zero, the data part of the message is empty.

  - *datatype*  
    A handle that represents the data type of the elements in the buffer.

  - *dest*  
    The rank of the destination process within the communicator *comm* parameter.

  - *tag*  
    The message tag that is used to distinguish different types of messages.

  - *comm*  
    The handle to the communicator.

  - *request* \[out\]  
    On return, a pointer to a handle that represents the communication operation.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

``` FORTRAN
    MPI_IRSEND(BUF, COUNT, DATATYPE, DEST, TAG, COMM, REQUEST, IERROR)
        <type> BUF(*)
        INTEGER COUNT, DATATYPE, DEST, TAG, COMM, REQUEST, IERROR
```

## Remarks

This function can return before the message was copied out of the send buffer. This function is local, it returns immediately, irrespective of the status of other processes. See the remarks for the [**MPI\_Rsend**](mpi-rsend-function.md) function for the description of the ready communication mode.

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

[**MPI\_Rsend**](mpi-rsend-function.md)

[**MPI\_Recv**](mpi-recv-function.md)

[**MPI\_Irecv**](mpi-irecv-function.md)

[**MPI\_Wait**](mpi-wait-function.md)

[**MPI\_Test**](mpi-test-function.md)

[**MPI\_Comm**](mpi-comm-enumeration.md)

[**MPI\_Datatype**](mpi-datatype-enumeration.md)

