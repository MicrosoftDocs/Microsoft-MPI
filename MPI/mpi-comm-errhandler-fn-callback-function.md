---
title: MPI_Comm_errhandler_fn callback function
TOCTitle: MPI_Comm_errhandler_fn callback function
ms:assetid: 07417db4-d087-42bf-a11c-ae1a3181c382
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473268(v=VS.85)
ms:contentKeyID: 59360814
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- COMM_ERRHANDLER_FUNCTION
- mpi/COMM_ERRHANDLER_FUNCTION
- mpi/MPI_Comm_errhandler_fn
- MPI_Comm_errhandler_fn
- mpif/COMM_ERRHANDLER_FUNCTION
- mpif/MPI_Comm_errhandler_fn
dev_langs:
- C++
- C
---

# MPI\_Comm\_errhandler\_fn callback function

*MPI\_Comm\_errhandler\_fn* is a placeholder for the application-defined function name.

## Syntax

``` c++
void MPI_Comm_errhandler_fn(
  _In_    MPI_Comm *comm,
  _Inout_ int      *errcode,
                   ...
);
```

## Parameters

  - *comm* \[in\]  
    TBD

  - *errcode* \[in, out\]  
    TBD

  - *...*  
    TBD

## Return value

TBD

## Fortran

    SUBROUTINE COMM_ERRHANDLER_FUNCTION(COMM, ERROR_CODE)
        INTEGER COMM, ERROR_CODE

## Remarks

The placeholder name of this function, *MPI\_Comm\_errhandler\_fn*, is deprecated in the MPI-2.2 standard and replaced by *MPI\_Comm\_errhandler\_function*. The function prototype is unchanged.

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
</tbody>
</table>


## See also

[MPI Management Functions](mpi-management-functions.md)

[**MPI\_Comm\_create\_errhandler**](mpi-comm-create-errhandler-function.md)

