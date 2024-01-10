---
title: MPI_Type_create_f90_complex function
TOCTitle: MPI_Type_create_f90_complex function
ms:assetid: a88fa355-14bb-4e57-9e5f-156552b747e6
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473488(v=VS.85)
ms:contentKeyID: 59361023
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_TYPE_CREATE_F90_COMPLEX
- mpif/MPI_Type_create_f90_complex
- mpi/MPI_TYPE_CREATE_F90_COMPLEX
dev_langs:
- C++
- C
---

# MPI\_Type\_create\_f90\_complex function

Return a predefined type that matches the specified range.

## Syntax

``` c++
int MPIAPI MPI_Type_create_f90_complex(
        int          p,
        int          r,
  _Out_ MPI_Datatype *newtype
);
```

## Parameters

  - *p*  
  - *r*  
    Decimal range desired.

  - *newtype* \[out\]  
    A predefine MPI Datatype that matches the range.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

``` FORTRAN
    MPI_TYPE_CREATE_F90_COMPLEX(P, R, NEWTYPE, IERROR)
        INTEGER P, R, NEWTYPE, IERROR
```

## Remarks

This function returns a predefined MPI datatype that matches a **COMPLEX** variable of **KIND** *selected\_real\_kind\(p, r\)*. Either *p* or *r* may be omitted from calls to *selected\_real\_kind\(p, r\)* (but not both). Analogously, either *p* or *r* may be set to **MPI\_UNDEFINED**. Matching rules for datatypes created by this function are analogous to the matching rules for datatypes created by **MPI\_TYPE\_CREATE\_F90_REAL**.

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

[MPI Miscellaneous Functions](mpi-miscellaneous-functions.md)

