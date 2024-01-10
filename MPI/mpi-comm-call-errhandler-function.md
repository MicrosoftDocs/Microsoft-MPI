---
title: MPI_Comm_call_errhandler function
TOCTitle: MPI_Comm_call_errhandler function
ms:assetid: 3d0aac27-1ec7-4f29-ad16-c6ef4c1ea8e7
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473257(v=VS.85)
ms:contentKeyID: 59360803
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_COMM_CALL_ERRHANDLER
- mpif/MPI_Comm_call_errhandler
- mpi/MPI_COMM_CALL_ERRHANDLER
dev_langs:
- C++
- C
description: Master Message Passing Interface (MPI) with MPI_Comm_Call_Errhandler Function. Learn error handling on communicators at Microsoft.
---

# MPI\_Comm\_call\_errhandler function

Call the error handler installed on a communicator.

## Syntax

``` c++
int MPIAPI MPI_Comm_call_errhandler(
   MPI_Comm comm,
   int      errorcode
);
```

## Parameters

  - *comm*  
    Communicator with error handler.

  - *errorcode*  
    Error code.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

``` FORTRAN
    MPI_COMM_CALL_ERRHANDLER(COMM, ERRORCODE, IERROR)
        INTEGER COMM, ERRORCODE, IERROR
```

## Remarks

Assuming the input parameters are valid, when the error handler is set to **MPI\_ERRORS\_RETURN**, this routine will always return **MPI\_SUCCESS**.

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

[MPI Management Functions](mpi-management-functions.md)

