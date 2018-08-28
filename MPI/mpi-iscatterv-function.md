---
title: MPI_Iscatterv function
TOCTitle: MPI_Iscatterv function
ms:assetid: 5675B3BF-395B-44B6-9CC0-A6DD9428974A
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Mt629170(v=VS.85)
ms:contentKeyID: 71965706
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_ISCATTERV
- mpif/MPI_Iscatterv
- mpi/MPI_ISCATTERV
dev_langs:
- C++
- C
api_location:
- Msmpi.dll
api_name:
- MPI_Iscatterv
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

# MPI\_Iscatterv function

## Syntax

``` c++
int MPIAPI MPI_Iscatterv(
  _In_opt_  const void         *sendbuf,
  _In_opt_  const int          sendcounts[],
  _In_opt_  const int          displs[],
  _In_            MPI_Datatype sendtype,
  _Out_opt_        void        *recvbuf,
  _In_            int          recvcount,
  _In_            MPI_Datatype recvtype,
  _In_            int          root,
  _In_            MPI_Comm     comm,
  _Out_           MPI_Request  *request
);
```

## Parameters

  - *sendbuf* \[in, optional\]  
    The pointer to a buffer that contains the data to be sent by the root process.
    
    This parameter is ignored for all non-root processes.
    
    If the *comm* parameter references an intracommunicator, you can specify an in-place option by specifying **MPI\_IN\_PLACE** in the root process. The *recvcount* and *recvtype* parameters are ignored. The scattered vector is still considered to contain *n* segments, where *n* is the group size; the segment that corresponds to the root process is not moved.

  - *sendcounts\[\]* \[in, optional\]  
    The number of elements to send to each process. If *sendcounts*\[*i*\] is zero, the data part of the message for that process is empty.
    
    This parameter is ignored for all non-root processes.

  - *displs\[\]* \[in, optional\]  
    The locations of the data to send to each communicator process. Each location in the array is relative to the corresponding element of the *sendbuf* array.
    
    In the *sendbuf*, *sendcounts*, and *displs* parameter arrays, the *n*th element of each array refers to the data to be sent to the *n*th communicator process.
    
    This parameter is significant only at the root process.

  - *sendtype* \[in\]  
    The data type of each element in the buffer.
    
    This parameter is ignored for all non-root processes.

  - *recvbuf* \[out, optional\]  
    The pointer to a buffer that contains the data that is received on each process. The number and data type of the elements in the buffer are specified in the *recvcount* and *recvtype* parameters.

  - *recvcount* \[in\]  
    The number of elements in the receive buffer. If the count is zero, the data part of the message is empty.

  - *recvtype* \[in\]  
    The data type of the elements in the receive buffer.

  - *root* \[in\]  
    The rank in the sending process within the specified communicator.

  - *comm* \[in\]  
    The [**MPI\_Comm**](mpi-comm-enumeration.md) communicator handle.

  - *request* \[out\]  
    The [**MPI\_Request**](mpi-comm-enumeration.md) handle representing the communication operation.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

    MPI_ISCATTERV(SENDBUF, SENDCOUNTS, DISPLS, SENDTYPE, RECVBUF, RECVCOUNT, RECVTYPE, ROOT, COMM, REQUEST, IERROR)
        <type> SENDBUF(*), RECVBUF(*)
        INTEGER SENDCOUNTS(*), DISPLS(*), SENDTYPE, RECVCOUNT, RECVTYPE, ROOT, COMM, REQUEST, IERROR

## Remarks

A non-blocking call initiates a collective reduction operation which must be completed in a separate completion call. Once initiated, the operation may progress independently of any computation or other communication at participating processes. In this manner, non-blocking reduction operations can mitigate possible synchronizing eﬀects of reduction operations by running them in the “background.”

All completion calls (e.g., [**MPI\_Wait)**](mpi-wait-function.md) are supported for non-blocking reduction operations.

## Requirements

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Product</p></td>
<td><p>Microsoft MPI v7</p></td>
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

[**MPI\_Datatype**](mpi-datatype-enumeration.md)

[**MPI\_Scatterv**](mpi-scatterv-function.md)

[**MPI\_Test**](mpi-test-function.md)

[**MPI\_Testall**](mpi-testall-function.md)

[**MPI\_Testany**](mpi-testany-function.md)

[**MPI\_Testsome**](mpi-testsome-function.md)

[**MPI\_Wait**](mpi-wait-function.md)

[**MPI\_Waitall**](mpi-waitall-function.md)

[**MPI\_Waitany**](mpi-waitany-function.md)

[**MPI\_Waitsome**](mpi-waitsome-function.md)

