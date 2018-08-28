---
title: MPI_Waitall function
TOCTitle: MPI_Waitall function
ms:assetid: 89393f53-3b4b-4427-9c66-a0d2732b56ed
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn520590(v=VS.85)
ms:contentKeyID: 59361061
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_WAITALL
- mpif/MPI_Waitall
- mpi/MPI_WAITALL
dev_langs:
- C++
- C
api_location:
- Msmpi.dll
api_name:
- MPI_Waitall
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

# MPI\_Waitall function

Completes multiple outstanding operations.

## Syntax

``` c++
int MPIAPI MPI_Waitall(
   int                              count,
   _Inout_count_(count) MPI_Request *array_of_requests,
   _Out_cap_(count) MPI_Status      *array_of_statuses
);
```

## Parameters

  - *count*  
    The number of entries in the *array\_of\_requests* parameter.

  - *array\_of\_requests*  
    An array of **MPI\_Request** handles of outstanding operations.

  - *array\_of\_statuses*  
    An array of [**MPI\_Status**](mpi-status-structure.md) objects that describe the completed operations. It might be **MPI\_STATUSES\_IGNORE** if no status information is requested.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

Returns **MPI\_ERR\_IN\_STATUS** if one or more operations are completed in error. The status of failed operations is returned in the corresponding entry in the *array\_of\_statuses* parameter.

In Fortran the return value is stored in the *IERROR* parameter.

## Fortran

    MPI_WAITALL(COUNT, ARRAY_OF_REQUESTS, INDEX, STATUS, IERROR)
        INTEGER COUNT, ARRAY_OF_REQUESTS, INDEX, STATUS(MPI_STATUS_SIZE), IERROR

## Remarks

This function is a non-local operation, successful completion might depend on matching operations at other processes.

A call to **MPI\_Waitall** returns when all of the operations that are associated with active requests in the *array\_of\_requests* array are completed. Any entries that are associated with persistent communication operations result in the persistent request are marked as inactive. Other operations are deallocated, and their corresponding entries in *array\_of\_requests* are set to **MPI\_REQUEST\_NULL**.

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

[**MPI\_Testall**](mpi-testall-function.md)

[**MPI\_Wait**](mpi-wait-function.md)

[**MPI\_Waitany**](mpi-waitany-function.md)

[**MPI\_Waitsome**](mpi-waitsome-function.md)

[**MPI\_Status**](mpi-status-structure.md)

