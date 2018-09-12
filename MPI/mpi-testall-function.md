---
title: MPI_Testall function
TOCTitle: MPI_Testall function
ms:assetid: 2509A007-140B-45B5-93B0-60A8987635B8
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473480(v=VS.85)
ms:contentKeyID: 59361015
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_TESTALL
- mpif/MPI_Testall
- mpi/MPI_TESTALL
dev_langs:
- C++
- C
api_location:
- Msmpi.dll
api_name:
- MPI_Testall
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

# MPI\_Testall function

Tests for the completion of all previously initiated requests.

## Syntax

``` c++
int MPIAPI MPI_Testall(
   int                              count,
   _Inout_count_(count) MPI_Request *array_of_requests,
   _Out_cap_(count) MPI_Status      *array_of_statuses
);
```

## Parameters

  - *count*  
    The number of entries in *array\_of\_requests* parameter.

  - *array\_of\_requests*  
    An array of **MPI\_Request** handles of outstanding operations.

  - *array\_of\_statuses*  
    An array of [**MPI\_Status**](mpi-status-structure.md) objects describing the completed operations. Might be **MPI\_STATUSES\_IGNORE** if no status information is desired.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

Returns **MPI\_ERR\_IN\_STATUS** if one or more operations complete in error. The status of failed operations is returned in the corresponding entry in the *array\_of\_statuses* parameter.

In Fortran the return value is stored in the *IERROR* parameter.

## Fortran

``` FORTRAN
    MPI_TESTALL(COUNT, ARRAY_OF_REQUESTS, FLAG, ARRAY_OF_STATUSES, IERROR)
        LOGICAL FLAG
        INTEGER COUNT, ARRAY_OF_REQUESTS(*),
        ARRAY_OF_STATUSES(MPI_STATUS_SIZE,*), IERROR
```

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

