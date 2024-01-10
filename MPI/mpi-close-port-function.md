---
title: MPI_Close_port function
TOCTitle: MPI_Close_port function
ms:assetid: 44452534-c82b-44ac-b39e-79f83a237add
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473252(v=VS.85)
ms:contentKeyID: 59360798
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_CLOSE_PORT
- mpif/MPI_Close_port
- mpi/MPI_CLOSE_PORT
dev_langs:
- C++
- C
---

# MPI\_Close\_port function

Close port.

## Syntax

``` c++
int MPIAPI MPI_Close_port(
  _In_ char *port_name
);
```

## Parameters

  - *port\_name* \[in\]  
    Port name.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

``` FORTRAN
    MPI_CLOSE_PORT(PORT_NAME, IERROR)
        CHARACTER*(*) PORT_NAME
        INTEGER IERROR
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

[MPI Process Management Functions](mpi-process-management-functions.md)

