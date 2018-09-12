---
title: MPI_Test function
TOCTitle: MPI_Test function
ms:assetid: a0f641d4-3764-43fe-969e-354a8857e5b5
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473479(v=VS.85)
ms:contentKeyID: 59361014
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_TEST
- mpif/MPI_Test
- mpi/MPI_TEST
dev_langs:
- C++
- C
api_location:
- Msmpi.dll
api_name:
- MPI_Test
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

# MPI\_Test function

Tests an outstanding operation for completion.

## Syntax

``` c++
int MPIAPI MPI_Test(
  _Inout_  MPI_Request *request,
  _Out_   int          *flag,
  _Out_   MPI_Status   *status
);
```

## Parameters

  - *request* \[in, out\]  
    A pointer to the **MPI\_Request** handle of an outstanding operation.

  - *flag* \[out\]  
    On return, contains a pointer to an integer that indicates whether the request is completed. A non-zero value indicates that the request is complete.

  - *status* \[out\]  
    On return, contains a pointer to an [**MPI\_Status**](mpi-status-structure.md) object that describes the specified operation if it is complete.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

``` FORTRAN
    MPI_WAIT(REQUEST, FLAG, STATUS, IERROR)
        LOGICAL FLAG
        INTEGER REQUEST, STATUS(MPI_STATUS_SIZE), IERROR
```

## Remarks

This function is a local operation. Successful completion does not depend on any operations at other processes.

If the operation that is associated with this request was a persistent communication operation, the persistent request is marked as inactive. Other operations are deallocated, and the request handle is set to **MPI\_REQUEST\_NULL**.

If the *request* parameter points to a value of **MPI\_REQUEST\_NULL** or to an inactive persistent request, then the function returns with the *flag* parameter set to a non-zero value and with the *status* parameter empty.

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

[**MPI\_Wait**](mpi-wait-function.md)

[**MPI\_Status**](mpi-status-structure.md)

[**MPI\_Testany**](mpi-testany-function.md)

[**MPI\_Testall**](mpi-testall-function.md)

[**MPI\_Testsome**](mpi-testsome-function.md)

