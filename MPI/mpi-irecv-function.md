---
title: MPI_Irecv function
TOCTitle: MPI_Irecv function
ms:assetid: 033ac026-a3a4-455f-9f4d-ba64ac7623e7
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473425(v=VS.85)
ms:contentKeyID: 59360961
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_IRECV
- mpif/MPI_Irecv
- mpi/MPI_IRECV
dev_langs:
- C++
- C
api_location:
- Msmpi.dll
api_name:
- MPI_Irecv
api_type:
- DLLExport
product:
- Windows
topic_type:
- apiref
- kbSyntax
product_family_name: VS
ROBOTS: INDEX,FOLLOW
description: Learn how to initiate a receive operation using MPI_Irecv function on Microsoft's platform. Understand syntax, parameters, and return values.
---

# MPI\_Irecv function

Initiates a receive operation and returns a handle to the requested communication operation.

## Syntax

``` c++
int MPIAPI MPI_Irecv(
  _In_opt_ void         *buf,
           int          count,
           MPI_Datatype datatype,
           int          source,
           int          tag,
           MPI_Comm     comm,
  _Out_    MPI_Request  *request
);
```

## Parameters

  - *buf* \[in, optional\]  
    A pointer to the buffer that contains the data to be sent.

  - *count*  
    The number of elements in the buffer array. If the data part of the message is empty, set the *count* parameter to 0.

  - *datatype*  
    The data type of the elements in the buffer.

  - *source*  
    The rank of the sending process within the specified communicator. Specify the **MPI\_ANY\_SOURCE** constant to specify that any source is acceptable.

  - *tag*  
    The message tag that can be used to distinguish different types of messages. Specify the **MPI\_ANY\_TAG** constant to indicate that any tag is acceptable.

  - *comm*  
    The handle to the communicator.

  - *request* \[out\]  
    On return, contains a handle to the requested communication operation.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

``` FORTRAN
    MPI_IRECV(BUF, COUNT, DATATYPE, SOURCE, TAG, COMM, REQUEST, IERROR)
        <type> BUF(*)
        INTEGER COUNT, DATATYPE, SOURCE, TAG, COMM, REQUEST, IERROR
```

## Remarks

This function is local, it returns immediately, and does not wait for any other process. This function can return before the message is received into the buffer.

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

[**MPI\_Recv**](mpi-recv-function.md)

[**MPI\_Wait**](mpi-wait-function.md)

[**MPI\_Test**](mpi-test-function.md)

[**MPI\_Comm**](mpi-comm-enumeration.md)

[**MPI\_Datatype**](mpi-datatype-enumeration.md)

