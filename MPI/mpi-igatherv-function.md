---
title: MPI_Igatherv function
TOCTitle: MPI_Igatherv function
ms:assetid: 7857E458-3F26-473E-9A37-F5F604B0EBA5
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Mt629168(v=VS.85)
ms:contentKeyID: 71965704
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_IGATHERV
- mpif/MPI_Igatherv
- mpi/MPI_IGATHERV
dev_langs:
- C++
- C
api_location:
- Msmpi.dll
api_name:
- MPI_Igatherv
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

# MPI\_Igatherv function

Gathers variable data from all members of a group to one member in a non-blocking way.

## Syntax

``` c++
int MPIAPI MPI_Igatherv(
  _In_opt_  const void         *sendbuf,
  _In_            int          sendcount,
  _In_            MPI_Datatype sendtype,
  _Out_opt_       void         *recvbuf,
  _In_opt_  const int          recvcounts[],
  _In_opt_  const int          displs[],
  _In_            MPI_Datatype recvtype,
  _In_            int          root,
  _In_            MPI_Comm     comm,
  _Out_           MPI_Request  *request
);
```

## Parameters

  - *sendbuf* \[in, optional\]  
    The handle to a buffer that contains the data to be sent to the root process.
    
    If the *comm* parameter references an intracommunicator, you can specify an in-place option by specifying **MPI\_IN\_PLACE** in all processes. The *sendcount* and *sendtype* parameters are ignored. Each process enters data in the corresponding receive buffer element. The *n*th process sends data to the *n*th element of the receive buffer. The data that is sent by the root process is assumed to be in the correct place in the receive buffer.

  - *sendcount* \[in\]  
    The number of elements in the send buffer. If *sendcount* is zero, the data part of the message is empty.

  - *sendtype* \[in\]  
    The data type of each element in the buffer.

  - *recvbuf* \[out, optional\]  
    The handle to a buffer on the root process that contains the data that is received from each process, including data that is sent by the root process. This parameter is significant only at the root process. The *recvbuf* parameter is ignored for all non-root processes.

  - *recvcounts\[\]* \[in, optional\]  
    The number of elements that is received from each process. Each element in the array corresponds to the rank of the sending process. If the count is zero, the data part of the message is empty. This parameter is significant only at the root process.

  - *displs\[\]* \[in, optional\]  
    The location, relative to the *recvbuf* parameter, of the data from each communicator process. The data that is received from process *j* is placed into the receive buffer of the root process offset *displs\[j\]* elements from the *sendbuf* pointer.
    
    In the *recvbuf*, *recvcounts*, and *displs* parameter arrays, the *n*th element of each array refers to the data that is received from the *n*th communicator process.
    
    This parameter is significant only at the root process.

  - *recvtype* \[in\]  
    The data type of each element in buffer. This parameter is significant only at the root process.

  - *root* \[in\]  
    The rank of the receiving process within the specified communicator.

  - *comm* \[in\]  
    The [**MPI\_Comm**](mpi-comm-enumeration.md) communicator handle.

  - *request* \[out\]  
    The [**MPI\_Request**](mpi-comm-enumeration.md) handle representing the communication operation.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

    MPI_IGATHERV(SENDBUF, SENDCOUNT, SENDTYPE, RECVBUF, RECVCOUNTS, DISPLS, RECVTYPE,
    ROOT, COMM, REQUEST, IERROR)
        <type> SENDBUF(*), RECVBUF(*)
        INTEGER SENDCOUNT, SENDTYPE, RECVCOUNTS(*), DISPLS(*), RECVTYPE, ROOT, COMM, REQUEST, IERROR

## Remarks

A non-blocking call initiates a collective reduction operation which must be completed in a separate completion call. Once initiated, the operation may progress independently of any computation or other communication at participating processes. In this manner, non-blocking reduction operations can mitigate possible synchronizing eﬀects of reduction operations by running them in the “background.”

All completion calls (e.g., [**MPI\_Wait**](mpi-wait-function.md)) are supported for non-blocking reduction operations.

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

[**MPI\_Gatherv**](mpi-gatherv-function.md)

[**MPI\_Test**](mpi-test-function.md)

[**MPI\_Testall**](mpi-testall-function.md)

[**MPI\_Testany**](mpi-testany-function.md)

[**MPI\_Testsome**](mpi-testsome-function.md)

[**MPI\_Wait**](mpi-wait-function.md)

[**MPI\_Waitall**](mpi-waitall-function.md)

[**MPI\_Waitany**](mpi-waitany-function.md)

[**MPI\_Waitsome**](mpi-waitsome-function.md)

