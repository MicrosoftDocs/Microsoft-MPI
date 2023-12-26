---
title: MPI_Ibcast function
TOCTitle: MPI_Ibcast function
ms:assetid: 2DBA6049-967D-41C1-A84C-942AE694A922
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn985828(v=VS.85)
ms:contentKeyID: 65288032
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_IBCAST
- mpif/MPI_Ibcast
- mpi/MPI_IBCAST
dev_langs:
- C++
- C
api_location:
- Msmpi.dll
api_name:
- MPI_Ibcast
api_type:
- DLLExport
product:
- Windows
topic_type:
- apiref
- kbSyntax
product_family_name: VS
ROBOTS: INDEX,FOLLOW
description: Learn about MPI_Ibcast function on Microsoft MPI. Understand its syntax, parameters, and usage for non-blocking message broadcasts in your processes.
---

# MPI\_Ibcast function

Broadcasts a message from the process with rank "root" to all other processes of the communicator in a non-blocking way.

## Syntax

``` c++
int MPIAPI MPI_Ibcast(
  _Inout_  void        *buffer,
  _In_    int          count,
  _In_    MPI_Datatype datatype,
  _In_    int          root,
  _In_    MPI_Comm     comm,
  _Out_   MPI_Request  *request
);
```

## Parameters

  - *buffer* \[in, out\]  
    The pointer to the data buffer. On the process that is specified by the *root* parameter, the buffer contains the data to be broadcast. On all other processes in the communicator that is specified by the *comm* parameter, the buffer receives the data broadcast by the root process. *buffer* consists of *count* successive elements of the **MPI\_Datatype** indicated by the *datatype* handle. The message length is specified in terms of number of elements, not number of bytes.

  - *count* \[in\]  
    The number of data elements in the buffer. If the *count* parameter is zero, the data part of the message is empty.

  - *datatype* \[in\]  
    The **MPI\_Datatype** handle representing the data type of each element in *buffer*.

  - *root* \[in\]  
    The rank of the process within the **MPI\_Comm** *comm* sending *buffer.*

  - *comm* \[in\]  
    The [**MPI\_Comm**](mpi-comm-enumeration.md) communicator handle.

  - *request* \[out\]  
    **MPI\_Request** handle representing the communication operation..

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

``` FORTRAN
    MPI_IBCAST(BUFFER, COUNT, DATATYPE, ROOT, COMM, REQUEST, IERROR)
        <type> BUFFER(*)  
        INTEGER COUNT, DATATYPE, ROOT, COMM, REQUEST, IERROR
```

## Remarks

A non-blocking call initiates a collective broadcast operation which must be completed in a separate completion call. Once initiated, the operation may progress independently of any computation or other communication at participating processes. In this manner, non-blocking broadcast operations can mitigate possible synchronizing eﬀects of broadcast operations by running them in the “background.”

All completion calls (e.g., [**MPI\_Wait**](mpi-wait-function.md)) are supported for non-blocking broadcast operations.

## Requirements

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Product</p></td>
<td><p>Microsoft MPI v6</p></td>
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

[MPI Collective Functions](mpi-collective-functions.md)

[**MPI\_Bcast**](mpi-bcast-function.md)

[**MPI\_Datatype**](mpi-datatype-enumeration.md)

[**MPI\_Test**](mpi-test-function.md)

[**MPI\_Testall**](mpi-testall-function.md)

[**MPI\_Testany**](mpi-testany-function.md)

[**MPI\_Testsome**](mpi-testsome-function.md)

[**MPI\_Wait**](mpi-wait-function.md)

[**MPI\_Waitall**](mpi-waitall-function.md)

[**MPI\_Waitany**](mpi-waitany-function.md)

[**MPI\_Waitsome**](mpi-waitsome-function.md)

[**MPI\_Comm**](mpi-comm-enumeration.md)

