---
title: MPI_Improbe function
TOCTitle: MPI_Improbe function
ms:assetid: 5761A549-EA87-4A8F-BE00-FFE5E8535BB7
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn985829(v=VS.85)
ms:contentKeyID: 65288033
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- mpi/MPI_Improbe
- mpi/MPI_IMPROBEV
- MPI_IMPROBE
- mpif/MPI_Improbe
dev_langs:
- C++
- C
api_location:
- Msmpi.dll
api_name:
- MPI_Improbe
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

# MPI\_Improbe function

Probes for a message in a non-blocking way. Provides a mechanism to receive the specific message that was matched regardless of intervening probe/receive operations. The matched message is de-queued off the receive queue, giving the application an opportunity to decide how to receive the message based on the information returned by the non-blocking matching probe operation. The matched message is then received using the [**MPI\_Mrecv**](mpi-mrecv-function.md) or [**MPI\_Imrecv**](mpi-imrecv-function.md) function.

## Syntax

``` c++
int MPIAPI MPI_Improbe(
  _In_  int         source,
  _In_  int         tag,
  _In_  MPI_Comm    comm,
  _Out_ Int         *flag,
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

  - *flag* \[out\]  
    On return, contains a pointer to an integer that indicates whether the specified *source*, *tag*, and *comm* are matched. A non-zero value indicates that the parameters are matched.

  - *message* \[out\]  
    On return, contains a pointer to the matched message.

  - *status* \[out\]  
    On return, contains a pointer to an [**MPI\_Status**](mpi-status-structure.md) structure where information about the message is stored.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

    MPI_IMPROBE(SOURCE, TAG, COMM, FLAG, MESSAGE, STATUS, IERROR)
          INTEGER SOURCE, TAG, COMM, FLAG, MESSAGE, STATUS(MPI_STATUS_SIZE), IERROR

## Remarks

This function returns *ﬂag* = **true** if there is a message that can be received and that matches the pattern speciﬁed by the arguments *source*, *tag*, and *comm*. The call matches the same message that would have been received by a call to [**MPI\_Recv**](mpi-recv-function.md) executed at the same point in the program and returns in status the same value that would have been returned by **MPI\_Recv**. In addition, it returns in *message* a handle to the matched message. Otherwise, the call returns *ﬂag* = **false** and leaves *status* and *message* undeﬁned.

## Requirements

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
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

[**MPI\_Mprobe**](mpi-mprobe-function.md)

[**MPI\_Recv**](mpi-recv-function.md)

[**MPI\_Imrecv**](mpi-imrecv-function.md)

