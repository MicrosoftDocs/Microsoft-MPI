---
title: MPI_Register_datarep function
TOCTitle: MPI_Register_datarep function
ms:assetid: 3c505756-3c1a-4284-b611-5bdda552819d
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473459(v=VS.85)
ms:contentKeyID: 59360994
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_REGISTER_DATAREP
- mpif/MPI_Register_datarep
- mpi/MPI_REGISTER_DATAREP
dev_langs:
- C++
- C
---

# MPI\_Register\_datarep function

TBD

## Syntax

``` c++
int MPIAPI MPI_Register_datarep(
  _In_     char                            *datarep,
  _In_opt_ MPI_Datarep_conversion_function *read_conversion_fn,
  _In_opt_ MPI_Datarep_conversion_function *write_conversion_fn,
  _In_     MPI_Datarep_extent_function     *dtype_file_extent_fn,
  _In_opt_ void                            *extra_state
);
```

## Parameters

  - *datarep* \[in\]  
    TBD

  - *read\_conversion\_fn* \[in, optional\]  
    TBD

  - *write\_conversion\_fn* \[in, optional\]  
    TBD

  - *dtype\_file\_extent\_fn* \[in\]  
    TBD

  - *extra\_state* \[in, optional\]  
    TBD

## Return value

TBD

## Fortran

    MPI_REGISTER_DATAREP(DATAREP, READ_CONVERSION_FN, WRITE_CONVERSION_FN,
                DTYPE_FILE_EXTENT_FN, EXTRA_STATE, IERROR)
        CHARACTER*(*) DATAREP
        EXTERNAL READ_CONVERSION_FN, WRITE_CONVERSION_FN, DTYPE_FILE_EXTENT_FN
        INTEGER(KIND=MPI_ADDRESS_KIND) EXTRA_STATE
        INTEGER IERROR

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

[MPI File Functions](mpi-file-functions.md)

[**MPI\_Datarep\_conversion\_function**](mpi-datarep-conversion-function-callback-function.md)

[**MPI\_Datarep\_extent\_function**](mpi-datarep-extent-function-callback-function.md)

