---
title: MPI_Unpublish_name function
TOCTitle: MPI_Unpublish_name function
ms:assetid: 427374d1-63f6-472a-9982-944dee4f945e
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn520587(v=VS.85)
ms:contentKeyID: 59361058
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_UNPUBLISH_NAME
- mpif/MPI_Unpublish_name
- mpi/MPI_UNPUBLISH_NAME
dev_langs:
- C++
- C
---

# MPI\_Unpublish\_name function

Unpublish a service name published with [**MPI\_Publish\_name**](mpi-publish-name-function.md).

## Syntax

``` c++
int MPIAPI MPI_Unpublish_name(
  _In_ char     *service_name,
       MPI_Info info,
  _In_ char     *port_name
);
```

## Parameters

  - *service\_name* \[in\]  
    Service name string.

  - *info*  
    Implementation-specific information.

  - *port\_name* \[in\]  
    Port name string.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

``` FORTRAN
    MPI_UNPUBLISH_NAME(SERVICE_NAME, INFO, PORT_NAME, IERROR)
        INTEGER INFO, IERROR
        CHARACTER*(*) SERVICE_NAME, PORT_NAME
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

[MPI Process Management Functions](mpi-process-management-functions.md)

