---
title: MPI_Comm_spawn function
TOCTitle: MPI_Comm_spawn function
ms:assetid: 99eaf029-0e82-4548-8132-eb8047cafc26
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473284(v=VS.85)
ms:contentKeyID: 59360830
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_COMM_SPAWN
- mpif/MPI_Comm_spawn
- mpi/MPI_COMM_SPAWN
dev_langs:
- C++
- C
description: Learn how to use the MPI_Comm_spawn function to spawn instances of an MPI application. Detailed syntax, parameters, and return values explained.
---

# MPI\_Comm\_spawn function

Spawns up to maxprocs instances of a single MPI application.

## Syntax

``` c++
int MPIAPI MPI_Comm_spawn(
  _In_  char                        *command,
  _In_  char                        *argv[],
        int                         maxprocs,
        MPI_Info                    info,
        int                         root,
        MPI_Comm                    comm,
  _Out_ MPI_Comm                    *intercomm,
        _Out_opt_cap_(maxprocs) int array_of_errcodes[]
);
```

## Parameters

  - *command* \[in\]  
    Name of program to be spawned.

  - *argv* \[in\]  
    Arguments to command.

  - *maxprocs*  
    Maximum number of processes to start.

  - *info*  
    A set of key-value pairs telling the runtime system where and how to start the processes.

  - *root*  
    Rank of process in which previous arguments are examined.

  - *comm*  
    Intracommunicator containing group of spawning processes.

  - *intercomm* \[out\]  
    Intercommunicator between original group and the newly spawned group.

  - *array\_of\_errcodes*  
    One code per process.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

``` FORTRAN
    MPI_COMM_SPAWN(COMMAND, ARGV, MAXPROCS, INFO, ROOT, COMM, INTERCOMM,
                ARRAY_OF_ERRCODES, IERROR)
        CHARACTER*(*) COMMAND, ARGV(*)
        INTEGER INFO, MAXPROCS, ROOT, COMM, INTERCOMM, ARRAY_OF_ERRCODES(*),
        IERROR
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

