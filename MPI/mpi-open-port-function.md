---
title: MPI_Open_port function
TOCTitle: MPI_Open_port function
ms:assetid: 1421cd0c-9be4-459c-bba3-d874ed1c7249
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473437(v=VS.85)
ms:contentKeyID: 59360973
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_OPEN_PORT
- mpif/MPI_Open_port
- mpi/MPI_OPEN_PORT
dev_langs:
- C++
- C
---

# MPI\_Open\_port function

TBD

## Syntax

``` c++
int MPIAPI MPI_Open_port(
   MPI_Info                          info,
   _Out_cap_(MPI_MAX_PORT_NAME) char *port_name
);
```

## Parameters

  - *info*  
    TBD

  - *port\_name*  
    TBD

## Return value

TBD

## Fortran

    MPI_OPEN_PORT(INFO, PORT_NAME, IERROR)
        CHARACTER*(*) PORT_NAME
        INTEGER INFO, IERROR

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

[MPI Process Management Functions](mpi-process-management-functions.md)

