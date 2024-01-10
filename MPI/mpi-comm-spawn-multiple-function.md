---
title: MPI_Comm_spawn_multiple function
TOCTitle: MPI_Comm_spawn_multiple function
ms:assetid: 138dbd80-1330-406f-abcb-6f95fa81135e
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473285(v=VS.85)
ms:contentKeyID: 59360831
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_COMM_SPAWN_MULTIPLE
- mpif/MPI_Comm_spawn_multiple
- mpi/MPI_COMM_SPAWN_MULTIPLE
dev_langs:
- C++
- C
description: Learn how to use the MPI_Comm_spawn_multiple function for spawning multiple binaries or the same binary with different arguments on Microsoft's official site.
---

# MPI\_Comm\_spawn\_multiple function

Spawns multiple binaries or the same binary with multiple sets of arguments, establishing communication with them and placing them in the same **MPI\_COMM\_WORLD**.

## Syntax

``` c++
int MPIAPI MPI_Comm_spawn_multiple(
            int                        count,
            _In_count_(count) char     *array_of_commands[],
            _In_opt_count_(count) char **array_of_argv[],
            _In_count_(count) int      array_of_maxprocs[],
            _In_count_(count) MPI_Info array_of_info[],
            int                        root,
            MPI_Comm                   comm,
  _Out_     MPI_Comm                   *intercomm,
  _Out_opt_ int                        array_of_errcodes[]
);
```

## Parameters

  - *count*  
    Number of commands.

  - *array\_of\_commands*  
    Programs to be executed.

  - *array\_of\_argv*  
    Arguments for commands.

  - *array\_of\_maxprocs*  
    Maximum number of processes to start for each command.

  - *array\_of\_info*  
    Info objects telling the runtime system where and how to start processes.

  - *root*  
    Rank of process in which previous arguments are examined.

  - *comm*  
    Intracommunicator containing group of spawning processes.

  - *intercomm* \[out\]  
    Intercommunicator between original group and newly spawned group.

  - *array\_of\_errcodes* \[out, optional\]  
    One error code per process.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

``` FORTRAN
    MPI_COMM_SPAWN_MULTIPLE(COUNT, ARRAY_OF_COMMANDS, ARRAY_OF_ARGV,
                ARRAY_OF_MAXPROCS, ARRAY_OF_INFO, ROOT, COMM, INTERCOMM,
                ARRAY_OF_ERRCODES, IERROR)
        INTEGER COUNT, ARRAY_OF_INFO(*), ARRAY_OF_MAXPROCS(*), ROOT, COMM,
        INTERCOMM, ARRAY_OF_ERRCODES(*), IERROR
        CHARACTER*(*) ARRAY_OF_COMMANDS(*), ARRAY_OF_ARGV(COUNT, *)
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

