---
title: MPI_Comm_size function
TOCTitle: MPI_Comm_size function
ms:assetid: de35aa91-5a27-41a7-9a26-ad0875c43390
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473283(v=VS.85)
ms:contentKeyID: 59360829
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_COMM_SIZE
- mpif/MPI_Comm_size
- mpi/MPI_COMM_SIZE
dev_langs:
- C++
- C
api_location:
- Msmpi.dll
api_name:
- MPI_Comm_size
api_type:
- DLLExport
product:
- Windows
topic_type:
- apiref
- kbSyntax
product_family_name: VS
ROBOTS: INDEX,FOLLOW
description: Learn how to use the MPI_Comm_size function to retrieve the number of processes in a communicator. Ideal for enhancing concurrency in your programs.
---

# MPI\_Comm\_size function

Retrieves the number of processes involved in a communicator, or the total number of processes available.

## Syntax

``` c++
int MPIAPI MPI_Comm_size(
        MPI_Comm comm,
  _Out_ int      *size
);
```

## Parameters

  - *comm*  
    The communicator to evaluate. Specify the **MPI\_COMM\_WORLD** constant to retrieve the total number of processes available.

  - *size* \[out\]  
    On return, indicates the number of processes in the group for the communicator.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

``` FORTRAN
    MPI_COMM_SIZE(COMM,SIZE,IERROR)
        INTEGER COMM, SIZE, IERROR
```

## Remarks

This function enables the user to retrieve the group size with a single function call. Otherwise, it would be necessary to create a temporary group by using the [**MPI\_Comm\_group**](mpi-comm-group-function.md) function, get the size of the group by using the [**MPI\_Group\_size**](mpi-group-size-function.md) function, and then free the temporary group by using the [**MPI\_Group\_free**](mpi-group-free-function.md) function.

This function is often used with the [**MPI\_Comm\_rank**](mpi-comm-rank-function.md) function to determine the amount of concurrency that is available for a specific library or program. The **MPI\_Comm\_rank** function indicates the rank of the process that calls it in the range from 0 to *size*-1, where *size* is retrieved by using the **MPI\_Comm\_size** function.

> [!NOTE]
> There is no standard way to change the number of processes after initialization has taken place.

 

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

[MPI Communicator Functions](mpi-communicator-functions.md)

[**MPI\_Comm\_rank**](mpi-comm-rank-function.md)

