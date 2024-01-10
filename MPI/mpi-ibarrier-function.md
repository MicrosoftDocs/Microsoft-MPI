---
title: MPI_Ibarrier function
TOCTitle: MPI_Ibarrier function
ms:assetid: F55E976F-7B43-4355-9471-F5DD66C64F4D
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn985827(v=VS.85)
ms:contentKeyID: 65288031
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_IBARRIER
- mpif/MPI_Ibarrier
- mpi/MPI_IBARRIER
dev_langs:
- C++
- C
api_location:
- Msmpi.dll
api_name:
- MPI_Ibarrier
api_type:
- DLLExport
product:
- Windows
topic_type:
- apiref
- kbSyntax
product_family_name: VS
ROBOTS: INDEX,FOLLOW
description: Learn about MPI_Ibarrier function, a non-blocking barrier synchronization method for group members. Understand syntax, parameters, and return values.
---

# MPI\_Ibarrier function

Performs a barrier synchronization across all members of a group in a non-blocking way.

## Syntax

``` c++
int MPIAPI MPI_Ibarrier(
  _In_  MPI_Comm    comm,
  _Out_ MPI_Request *request
);
```

## Parameters

  - *comm* \[in\]  
    **MPI\_COMM** communicator handle.

  - *request* \[out\]  
    **MPI\_Request** handle representing the communication operation.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

``` FORTRAN
    MPI_IBARRIER(COMM, REQUEST, IERROR)
        INTEGER COMM, REQUEST, IERROR
```

## Remarks

A non-blocking call initiates a collective barrier operation which must be completed in a separate completion call. Once initiated, the operation may progress independently of any computation or other communication at participating processes. In this manner, non-blocking barrier operations can mitigate possible synchronizing eﬀects of barrier operations by running them in the “background.”

All completion calls (e.g., [**MPI\_Wait**](mpi-wait-function.md)) are supported for non-blocking barrier operations.

## Requirements

<table>
<colgroup>
<col  />
<col  />
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

[**MPI\_Barrier**](mpi-barrier-function.md)

[**MPI\_Test**](mpi-test-function.md)

[**MPI\_Testall**](mpi-testall-function.md)

[**MPI\_Testany**](mpi-testany-function.md)

[**MPI\_Testsome**](mpi-testsome-function.md)

[**MPI\_Wait**](mpi-wait-function.md)

[**MPI\_Waitall**](mpi-waitall-function.md)

[**MPI\_Waitany**](mpi-waitany-function.md)

[**MPI\_Waitsome**](mpi-waitsome-function.md)

[**MPI\_Comm**](mpi-comm-enumeration.md)

