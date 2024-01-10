---
title: MPI_File_write_all_end function
TOCTitle: MPI_File_write_all_end function
ms:assetid: d9ec9d1a-e525-4cf7-8fb6-62234efaba92
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473363(v=VS.85)
ms:contentKeyID: 59360899
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_FILE_WRITE_ALL_END
- mpif/MPI_File_write_all_end
- mpi/MPI_FILE_WRITE_ALL_END
dev_langs:
- C++
- C
---

# MPI\_File\_write\_all\_end function

Completes a split collective write using individual file pointer.

## Syntax

``` c++
int MPIAPI MPI_File_write_all_end(
        MPI_File   file,
  _In_  void       *buf,
  _Out_ MPI_Status *status
);
```

## Parameters

  - *file*  
    File handle.

  - *buf* \[in\]  
    Initial address of buffer.

  - *status* \[out\]  
    Status object.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

``` FORTRAN
    MPI_FILE_WRITE_ALL_END(FH, BUF, STATUS, IERROR)
        <type> BUF(*)
        INTEGER FH, STATUS(MPI_STATUS_SIZE), IERROR
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

[MPI File Functions](mpi-file-functions.md)

