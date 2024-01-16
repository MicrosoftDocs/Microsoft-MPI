---
title: MPI_Mprobe function
TOCTitle: MPI_Mprobe function
ms:assetid: A54B0A78-045E-4D90-AC91-761893AD8DB5
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn985832(v=VS.85)
ms:contentKeyID: 65288036
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- mpi/MPI_Mprobe
- mpi/MPI_MPROBEV
- MPI_MPROBE
- mpif/MPI_Mprobe
dev_langs:
- C++
- C
api_location:
- Msmpi.dll
api_name:
- MPI_Mprobe
api_type:
- DLLExport
product:
- Windows
topic_type:
- apiref
- kbSyntax
product_family_name: VS
ROBOTS: INDEX,FOLLOW
description: Learn about the MPI_Mprobe function on Microsoft MPI v6. Understand its syntax, parameters, return value, and how it provides a mechanism for message passing.
---

# MPI\_Mprobe function

Blocking probes for a message. Provides a mechanism to receive the specific message that was matched regardless of intervening probe/receive operations. The matched message is de-queued off the receive queue, giving the application an opportunity to decide how to receive the message based on the information returned by the matching probe operation. The matched message is then received using the [**MPI\_Mrecv**](mpi-mrecv-function.md) or [**MPI\_Imrecv**](mpi-imrecv-function.md) function.

## Syntax

``` c++
int MPIAPI MPI_Mprobe(
  _In_  int         source,
  _In_  int         tag,
  _In_  MPI_Comm    comm,
  _Out_ MPI_Message *message,
  _Out_ MPI_Status  *status
);
```

## Parameters

  - *source* \[in\]  
    Source rank or **MPI\_ANY\_SOURCE**.

  - *tag* \[in\]  
    Message tag or **MPI\_ANY\_TAG**.

  - *comm* \[in\]  
    MPI communicator handle.

  - *message* \[out\]  
    On return, contains a pointer to the matched message.

  - *status* \[out\]  
    On return, contains a pointer to an [**MPI\_Status**](mpi-status-structure.md) structure where information about the message is stored.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

``` FORTRAN
    MPI_MPROBE(SOURCE, TAG, COMM, MESSAGE, STATUS, IERROR)
          INTEGER SOURCE, TAG, COMM, MESSAGE, STATUS(MPI_STATUS_SIZE), IERROR
```

## Remarks

This function behaves like [**MPI\_Improbe**](mpi-improbe-function.md) except that it is a blocking call that returns only after a matching message has been found.

## Requirements

<table>
<colgroup>
<col/>
<col/>
</colgroup>
<tbody>
<tr class="odd">
<td><p>Product</p></td>
<td><p>Microsoft MPI v6</p></td>
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

[MPI Point to Point Functions](mpi-point-to-point-functions.md)

[**MPI\_Improbe**](mpi-improbe-function.md)

[**MPI\_Recv**](mpi-recv-function.md)

[**MPI\_Imrecv**](mpi-imrecv-function.md)

