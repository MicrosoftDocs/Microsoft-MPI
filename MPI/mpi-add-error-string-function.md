---
title: MPI_Add_error_string function
TOCTitle: MPI_Add_error_string function
ms:assetid: 20bd7d14-41a0-4ecc-bdd5-4ccd9b889447
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn502499(v=VS.85)
ms:contentKeyID: 59360771
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_ADD_ERROR_STRING
- mpif/MPI_Add_error_string
- mpi/MPI_ADD_ERROR_STRING
dev_langs:
- C++
- C
---

# MPI\_Add\_error\_string function

Associate an error string with an MPI error code or class

## Syntax

``` c++
int MPIAPI MPI_Add_error_string(
   int         errorcode,
   _In_z_ char *string
);
```

## Parameters

  - *errorcode*  
    Error code or class.

  - *string*  
    Text corresponding to errorcode.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

``` FORTRAN
    MPI_ADD_ERROR_STRING(ERRORCODE, STRING, IERROR)
        INTEGER ERRORCODE, IERROR
        CHARACTER*(*) STRING
```

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

[MPI Management Functions](mpi-management-functions.md)

