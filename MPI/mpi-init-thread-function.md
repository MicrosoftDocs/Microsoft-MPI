---
title: MPI_Init_thread function
TOCTitle: MPI_Init_thread function
ms:assetid: 8042dcc8-8099-446f-85a0-9fbffa8f487e
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473421(v=VS.85)
ms:contentKeyID: 59360957
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_INIT_THREAD
- mpif/MPI_Init_thread
- mpi/MPI_INIT_THREAD
dev_langs:
- C++
- C
api_location:
- Msmpi.dll
api_name:
- MPI_Init_thread
api_type:
- DLLExport
product:
- Windows
topic_type:
- apiref
- kbSyntax
product_family_name: VS
ROBOTS: INDEX,FOLLOW
---

# MPI\_Init\_thread function

Initializes the calling MPI process’s execution environment for threaded execution.

## Syntax

``` c++
int MPIAPI MPI_Init_thread(
  _In_opt_ int                        *argc,
           _In_opt_count_(*argc) char ***argv,
  _In_     int                        required,
  _Out_    int                        *provided
);
```

## Parameters

  - *argc* \[in, optional\]  
    A pointer to the number of arguments for the program. This value can be NULL.

  - *argv* \[optional\]  
    A pointer to the argument list for the program. This value can be NULL.

  - *required* \[in\]  
    The level of desired thread support. Multiple MPI processes in the same job may use different values.
    
    <table>
    <tbody>
    <tr class="odd">
    <td>MPI_THREAD_SINGLE</td>
    <td>Only a single thread in the program will execute.</td>
    </tr>
    <tr class="even">
    <td>MPI_THREAD_FUNNELED</td>
    <td>The process may contain multiple threads, but the thread that called <strong>MPI_Init_thread</strong> is the only one that makes MPI function calls.</td>
    </tr>
    <tr class="odd">
    <td>MPI_THREAD_SERIALIZED</td>
    <td>The process may contain multiple threads, and all of those threads may make MPI function calls, but only one at a time.</td>
    </tr>
    <tr class="even">
    <td>MPI_THREAD_MULTIPLE</td>
    <td>Multiple application threads may call MPI functions with no restrictions. This value is currently only supported on MS-MPI V6 running on Windows Server 2012, Windows Server 2012 R2, Windows 8, and Windows 8.1.</td>
    </tr>
    </tbody>
    </table>
    
     

  - *provided* \[out\]  
    The level of provided thread support. The value returned will be from the table above.
    
     

## Return value

**MPI\_SUCCESS** if the function returns successfully. Other error codes if the call failed for other reasons (such as invalid arguments).

In Fortran the return value is stored in the *IERROR* parameter.

## Fortran

``` FORTRAN
    MPI_INIT_THREAD(REQUIRED, PROVIDED, IERROR)
        INTEGER REQUIRED, PROVIDED, IERROR
```

## Remarks

This function must be called by one thread only. That thread will be known as the “Main Thread” and must be the same thread to call [**MPI\_Finalize**](mpi-finalize-function.md).

The Fortran binding of **MPI\_Init\_thread** does not accept the ARGC and ARGV parameters.

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

[MPI External Functions](mpi-external-functions.md)

[**MPI\_Finalize**](mpi-finalize-function.md)

[**MPI\_Init**](mpi-init-function.md)

