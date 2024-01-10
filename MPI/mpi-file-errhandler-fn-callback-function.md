---
title: MPI_File_errhandler_fn callback function
TOCTitle: MPI_File_errhandler_fn callback function
ms:assetid: ae5f7495-3285-4d2a-9c67-9f186c35babf
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473308(v=VS.85)
ms:contentKeyID: 59360854
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- mpi/MPI_File_errhandler_fn
- MPI_File_errhandler_fn
- mpif/MPI_File_errhandler_fn
dev_langs:
- C++
- C
---

# MPI\_File\_errhandler\_function callback function

*MPI\_File\_errhandler\_function* is a placeholder for the application-defined function name.

## Syntax

``` c++
void MPI_File_errhandler_function(
  _In_    MPI_File *file,
  _Inout_  int     *errcode,
                   ...
);
```

## Parameters

  - *file* \[in\]  
    File in use.

  - *errcode* \[in, out\]  
    Error code to be returned.

  - *...*  

## Fortran

``` FORTRAN
    SUBROUTINE FILE_ERRHANDLER_FUNCTION(FILE, ERROR_CODE)
    INTEGER FILE, ERROR_CODE
```

## Remarks

The placeholder name of this function, *MPI\_File\_errhandler\_fn*, is deprecated in the MPI-2.2 standard and replaced by *MPI\_File\_errhandler\_function*. The function prototype is unchanged.

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
</tbody>
</table>


## See also

[MPI Management Functions](mpi-management-functions.md)

[**MPI\_File\_create\_errhandler**](mpi-file-create-errhandler-function.md)

