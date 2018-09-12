---
title: MPI_Wait function
TOCTitle: MPI_Wait function
ms:assetid: 516ab401-2b6b-45db-9815-34d75b9c4c3b
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn520589(v=VS.85)
ms:contentKeyID: 59361060
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_WAIT
- mpif/MPI_Wait
- mpi/MPI_WAIT
dev_langs:
- C++
- C
api_location:
- Msmpi.dll
api_name:
- MPI_Wait
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

# MPI\_Wait function

Completes an outstanding operation.

## Syntax

``` c++
int MPIAPI MPI_Wait(
  _Inout_ MPI_Request *request,
  _Out_   MPI_Status  *status
);
```

## Parameters

  - *request* \[in, out\]  
    A pointer to the **MPI\_Request** handle of an outstanding operation.

  - *status* \[out\]  
    A pointer to an [**MPI\_Status**](mpi-status-structure.md) object that describes the specified request.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

``` FORTRAN
    MPI_WAIT(REQUEST, STATUS, IERROR)
        INTEGER REQUEST, STATUS(MPI_STATUS_SIZE), IERROR
```

## Remarks

This function is a non-local operation. Successful completion might depend on matching operations at other processes.

This function returns when the operation that is identified by the *request* parameter is completed.

If the operation that is associated with this request was a persistent communication operation, the persistent request is marked as inactive. Other operations are deallocated, and the request handle is set to **MPI\_REQUEST\_NULL**.

If the *request* parameter points to a value of **MPI\_REQUEST\_NULL** or to an inactive persistent communication request, then the function returns an empty status.

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

[**MPI\_Isend**](mpi-isend-function.md)

[**MPI\_Ibsend**](mpi-ibsend-function.md)

