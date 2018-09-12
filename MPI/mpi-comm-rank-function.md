---
title: MPI_Comm_rank function
TOCTitle: MPI_Comm_rank function
ms:assetid: f42f18ed-4a0a-4c4a-b5a8-11bb8ad8a0b9
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473277(v=VS.85)
ms:contentKeyID: 59360823
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_COMM_RANK
- mpif/MPI_Comm_rank
- mpi/MPI_COMM_RANK
dev_langs:
- C++
- C
api_location:
- Msmpi.dll
api_name:
- MPI_Comm_rank
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

# MPI\_Comm\_rank function

Retrieves the rank of the calling process in the group of the specified communicator.

## Syntax

``` c++
int MPIAPI MPI_Comm_rank(
        MPI_Comm comm,
  _Out_ int      *rank
);
```

## Parameters

  - *comm*  
    The communicator.

  - *rank* \[out\]  
    On return, a pointer to the identifier of the calling process within the group of the communicator.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

``` FORTRAN
    MPI_COMM_RANK(COMM,RANK,IERROR)
        INTEGER COMM, RANK, IERROR
```

## Remarks

This function enables the user to retrieve the process rank with a single function call. Otherwise, it would be necessary to create a temporary group by using the [**MPI\_Comm\_group**](mpi-comm-group-function.md) function, get the rank in the group by using the [**MPI\_Group\_rank**](mpi-group-rank-function.md) function, and then free the temporary group by using the [**MPI\_Group\_free**](mpi-group-free-function.md) function.

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

[MPI Communicator Functions](mpi-communicator-functions.md)

[**MPI\_Comm\_size**](mpi-comm-size-function.md)

