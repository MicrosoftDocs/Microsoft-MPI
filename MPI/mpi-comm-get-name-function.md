---
title: MPI_Comm_get_name function
TOCTitle: MPI_Comm_get_name function
ms:assetid: a842a324-3e85-4a75-85dc-4eb6bf5f80a6
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473273(v=VS.85)
ms:contentKeyID: 59360819
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_COMM_GET_NAME
- mpif/MPI_Comm_get_name
- mpi/MPI_COMM_GET_NAME
dev_langs:
- C++
- C
description: Learn how to use the MPI_Comm_get_name function to return the print name from the communicator. Detailed syntax, parameters, and return values explained.
---

# MPI\_Comm\_get\_name function

Return the print name from the communicator.

## Syntax

``` c++
int MPIAPI MPI_Comm_get_name(
        MPI_Comm                                                    comm,
        _Out_z_cap_post_count_(MPI_MAX_OBJECT_NAME,*resultlen) char *comm_name,
  _Out_ int                                                         *resultlen
);
```

## Parameters

  - *comm*  
    Communicator to get name of.

  - *comm\_name*  
    On output, contains the name of the communicator. It must be an array of size at least **MPI\_MAX\_OBJECT\_NAME**.

  - *resultlen* \[out\]  
    Number of characters in name.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

``` FORTRAN
    MPI_COMM_GET_NAME(COMM, COMM_NAME, RESULTLEN, IERROR)
        INTEGER COMM, RESULTLEN, IERROR
        CHARACTER*(*) COMM_NAME
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

[MPI Miscellaneous Functions](mpi-miscellaneous-functions.md)

