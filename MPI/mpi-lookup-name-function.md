---
title: MPI_Lookup_name function
TOCTitle: MPI_Lookup_name function
ms:assetid: 8524b3c6-6141-402b-a1e8-4c61462ce763
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473432(v=VS.85)
ms:contentKeyID: 59360968
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_LOOKUP_NAME
- mpif/MPI_Lookup_name
- mpi/MPI_LOOKUP_NAME
dev_langs:
- C++
- C
---

# MPI\_Lookup\_name function

TBD

## Syntax

``` c++
int MPIAPI MPI_Lookup_name(
   _In_z_ char                       *service_name,
   MPI_Info                          info,
   _Out_cap_(MPI_MAX_PORT_NAME) char *port_name
);
```

## Parameters

  - *service\_name*  
    TBD

  - *info*  
    TBD

  - *port\_name*  
    TBD

## Return value

TBD

## Fortran

    MPI_LOOKUP_NAME(SERVICE_NAME, INFO, PORT_NAME, IERROR)
        CHARACTER*(*) SERVICE_NAME, PORT_NAME
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

