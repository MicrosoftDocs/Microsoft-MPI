---
title: MPI_Waitany function
TOCTitle: MPI_Waitany function
ms:assetid: bb03d8e6-8af9-43aa-a4b9-c7ff50d6fb22
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn520591(v=VS.85)
ms:contentKeyID: 59361062
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_WAITANY
- mpif/MPI_Waitany
- mpi/MPI_WAITANY
dev_langs:
- C++
- C
api_location:
- Msmpi.dll
api_name:
- MPI_Waitany
api_type:
- DLLExport
product:
- Windows
topic_type:
- apiref
- kbSyntax
product_family_name: VS
ROBOTS: INDEX,FOLLOW
description: Learn about the MPI_Waitany function, its syntax, parameters, and return values. Enhance your knowledge of MPI Point to Point Functions.
---

# MPI\_Waitany function

Completes one out of several outstanding operations.

## Syntax

``` c++
int MPIAPI MPI_Waitany(
        int                              count,
        _Inout_count_(count) MPI_Request *array_of_requests,
  _Out_ int                              *index,
  _Out_ MPI_Status                       *status
);
```

## Parameters

  - *count*  
    The number of entries in the *array\_of\_requests* parameter.

  - *array\_of\_requests*  
    An array of **MPI\_Request** handles of outstanding operations.

  - *index* \[out\]  
    A pointer to an integer that indicates the index in the *array\_of\_requests* parameter of the operation that is completed. The array is indexed from zero in C, and from one in Fortran.

  - *status* \[out\]  
    A pointer to an [**MPI\_Status**](mpi-status-structure.md) object that describes the completed operation.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

``` FORTRAN
    MPI_WAITANY(COUNT, ARRAY_OF_REQUESTS, INDEX, STATUS, IERROR)
        INTEGER COUNT, ARRAY_OF_REQUESTS, INDEX, STATUS(MPI_STATUS_SIZE), IERROR
```

## Remarks

This function is a non-local operation. Successful completion might depend on matching operations at other processes.

This function returns when one of the operations that is associated with active requests in the *array\_of\_requests* parameter is completed. If more than one outstanding operation is completed, one is arbitrarily chosen. If the completed operation is a persistent communication operation, the persistent request is marked as inactive. A nonpersistent operation is deallocated, and its corresponding entry in the *array\_of\_requests* parameter is set to **MPI\_REQUEST\_NULL**.

Entries in the *array\_of\_requests* parameter can be **MPI\_REQUEST\_NULL** or a handle to an inactive persistent communication request. If the *count* parameter is zero, or all entries in *array\_of\_requests* are **MPI\_REQUEST\_NULL** or inactive persistent communication requests, then the function returns immediately with the *index* parameter set to **MPI\_UNDEFINED** and an empty status.

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

[**MPI\_Testany**](mpi-testany-function.md)

[**MPI\_Wait**](mpi-wait-function.md)

[**MPI\_Waitall**](mpi-waitall-function.md)

[**MPI\_Waitsome**](mpi-waitsome-function.md)

[**MPI\_Status**](mpi-status-structure.md)

