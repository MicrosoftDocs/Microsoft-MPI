---
title: MPI_Ibsend function
TOCTitle: MPI_Ibsend function
ms:assetid: 3d745753-698a-4f0a-99b3-27d79c1a888a
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473408(v=VS.85)
ms:contentKeyID: 59360944
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_IBSEND
- mpif/MPI_Ibsend
- mpi/MPI_IBSEND
dev_langs:
- C++
- C
api_location:
- Msmpi.dll
api_name:
- MPI_Ibsend
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

# MPI\_Ibsend function

Initiates a buffered mode send operation and returns a handle to the communication operation.

## Syntax

``` c++
int MPIAPI MPI_Ibsend(
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

  - *request* \[out\]  
    On return, contains a handle to the requested communication operation.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

``` FORTRAN
    MPI_IBSEND(BUF, COUNT, DATATYPE, DEST, TAG, COMM, REQUEST, IERROR)
        <type> BUF(*)
        INTEGER COUNT, DATATYPE, DEST, TAG, COMM, REQUEST, IERROR
```

## Remarks

This function is local, it returns immediately, and does not wait for any other process. This function can return before the message is copied out of the send buffer.

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

[**MPI\_Recv**](mpi-recv-function.md)

[**MPI\_Irecv**](mpi-irecv-function.md)

[**MPI\_Wait**](mpi-wait-function.md)

[**MPI\_Test**](mpi-test-function.md)

[**MPI\_Comm**](mpi-comm-enumeration.md)

[**MPI\_Datatype**](mpi-datatype-enumeration.md)

