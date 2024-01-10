---
title: MPI_Error_string function
TOCTitle: MPI_Error_string function
ms:assetid: 8809420b-8081-4057-a422-a6abc1f19dd4
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473300(v=VS.85)
ms:contentKeyID: 59360846
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- mpi/MPI_Error_string
- mpi/MPI_FILE_CALL_ERRHANDLER
- MPI_ERROR_STRING
- mpif/MPI_Error_string
- mpif/MPI_FILE_CALL_ERRHANDLER
dev_langs:
- C++
- C
---

# MPI\_Error\_string function

Returns a string for a given error code.

## Syntax

``` c++
int MPIAPI MPI_Error_string(
        int                                                          errorcode,
        _Out_z_cap_post_count_(MPI_MAX_ERROR_STRING,*resultlen) char *string,
  _Out_ int                                                          *resultlen
);
```

## Parameters

  - *errorcode*  
    Error code returned by an MPI routine or an MPI error class.

  - *string*  
    Text that corresponds to the errorcode.

  - *resultlen* \[out\]  
    Length of string.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

``` FORTRAN
    MPI_ERROR_STRING(ERRORCODE, STRING, RESULTLEN, IERROR)
        INTEGER ERRORCODE, RESULTLEN, IERROR
        CHARACTER*(*) STRING
```

## Requirements

<table>
<colgroup>
<col  />
<col  />
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

