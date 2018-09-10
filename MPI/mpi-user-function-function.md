---
title: MPI_User_function function
TOCTitle: MPI_User_function function
ms:assetid: 81f4f323-be56-4546-b589-9f1a0aae1515
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn520588(v=VS.85)
ms:contentKeyID: 59361059
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- mpi/MPI_User_function
- mpi/USER_FUNCTION
- MPI_User_function
- mpif/MPI_User_function
- mpif/USER_FUNCTION
- USER_FUNCTION
dev_langs:
- C++
- C
---

# MPI\_User\_function function

**MPI\_User\_function** is a placeholder for the application-defined function name.

## Syntax

``` c++
void MPI_User_function(
       _In_count_   invec,
       _Inout_ void *inoutvec,
  _In_ int          *len,
  _In_ MPI_Datatype *datatype
);
```

## Parameters

  - *invec*  
    Array of elements that the user function is combining.

  - *inoutvec*  
    Array of elements that the user function is combining.

  - *len* \[in\]  
    Length of *invec* and *inoutvec*.

  - *datatype* \[in\]  
    A handle to the data type that was passed into the call to [**MPI\_Reduce**](mpi-reduce-function.md).

## Return value

TBD

## Fortran

    SUBROUTINE USER_FUNCTION(INVEC, INOUTVEC, LEN, DATATYPE)
        <type> INVEC(LEN), INOUTVEC(LEN)
        INTEGER LEN, DATATYPE

## Remarks

The user-defined operation is assumed to be associative. If *commute = true*, then the operation should be both commutative and associative. If *commute = false*, then the order of operands is fixed and is defined to be in ascending, process rank order, beginning with process zero. The order of evaluation can be changed, taking advantage of the associativity of the operation. If *commute = true* then the order of evaluation can be changed, taking advantage of commutativity and associativity.

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

[MPI Collective Functions](mpi-collective-functions.md)

[**MPI\_Op\_create**](mpi-op-create-function.md)

