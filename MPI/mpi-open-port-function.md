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
description: Learn how to establish connections between MPI processes using the MPI_Open_port function. Includes syntax, parameters, and return values.
---

# MPI\_Open\_port function

Establishes an address that can be used to establish connections between groups of MPI processes.

## Syntax

``` c++
int MPIAPI MPI_Open_port(
   MPI_Info                          info,
   _Out_cap_(MPI_MAX_PORT_NAME) char *port_name
);
```

## Parameters

  - *info*  
    Implementation-specific information on how to establish a port for [**MPI\_Comm\_accept**](mpi-comm-accept-function.md).

  - *port\_name*  
    Newly established port.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

``` FORTRAN
    MPI_OPEN_PORT(INFO, PORT_NAME, IERROR)
        CHARACTER*(*) PORT_NAME
        INTEGER INFO, IERROR
```

## Remarks

MPI copies a system-supplied port name into *port_name*. *port_name* identifies the newly opened port and can be used by a client to contact the server. The maximum size string that may be supplied by the system is **MPI\_MAX\_PORT\_NAME**.

Reserved Info Key Values:
- ip_port - Value contains IP port number at which to establish a port.
- ip_address - Value contains IP address at which to establish a port.

If the address is not a valid IP address of the host on which the [**MPI\_Open\_port**](mpi-open-port-function.md) call is made, the results are undefined.

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

