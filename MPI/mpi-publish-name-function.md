---
title: MPI_Publish_name function
TOCTitle: MPI_Publish_name function
ms:assetid: 456bdd5f-8597-451f-8202-9ba6a610bfc3
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473450(v=VS.85)
ms:contentKeyID: 59360985
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_PUBLISH_NAME
- mpif/MPI_Publish_name
- mpi/MPI_PUBLISH_NAME
dev_langs:
- C++
- C
description: Learn how to use the MPI_Publish_name function for service name publishing with MPI_Comm_connect on Microsoft's official site.
---

# MPI\_Publish\_name function

Publish a service name for use with [**MPI\_Comm\_connect**](mpi-comm-connect-function.md).

## Syntax

``` c++
int MPIAPI MPI_Publish_name(
  _In_ char     *service_name,
       MPI_Info info,
  _In_ char     *port_name
);
```

## Parameters

  - *service\_name* \[in\]  
    Service name to associate with the port.

  - *info*  
    Implementation-specific information.

  - *port\_name* \[in\]  
    Port name.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

``` FORTRAN
    MPI_PUBLISH_NAME(SERVICE_NAME, INFO, PORT_NAME, IERROR)
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

