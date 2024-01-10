---
title: MPI_Scatterv function
TOCTitle: MPI_Scatterv function
ms:assetid: 057f380a-db02-4197-a4e8-e0e0e8fd2dea
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473466(v=VS.85)
ms:contentKeyID: 59361001
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_SCATTERV
- mpif/MPI_Scatterv
- mpi/MPI_SCATTERV
dev_langs:
- C++
- C
api_location:
- Msmpi.dll
api_name:
- MPI_Scatterv
api_type:
- DLLExport
product:
- Windows
topic_type:
- apiref
- kbSyntax
product_family_name: VS
ROBOTS: INDEX,FOLLOW
description: Learn how to use the MPI_Scatterv function to scatter data across all members of a group. Detailed syntax, parameters, and return values explained.
---

# MPI\_Scatterv function

Scatters data from one member across all members of a group. The **MPI\_Scatterv** function performs the inverse of the operation that is performed by the [**MPI\_Gatherv**](mpi-gatherv-function.md) function.

## Syntax

``` c++
int MPIAPI MPI_Scatterv(
  _In_  void         *sendbuf,
  _In_  int          *sendcounts,
  _In_  int          *displs,
        MPI_Datatype sendtype,
  _Out_ void         *recvbuf,
        int          recvcount,
        MPI_Datatype recvtype,
        int          root,
        MPI_Comm     comm
);
```

## Parameters

  - *sendbuf* \[in\]  
    The pointer to a buffer that contains the data to be sent by the root process.
    
    The *sendbuf* parameter is ignored for all non-root processes.
    
    If the *comm* parameter references an intracommunicator, you can specify an in-place option by specifying **MPI\_IN\_PLACE** in the root process. The *recvcount* and *recvtype* parameters are ignored. The scattered vector is still considered to contain *n* segments, where *n* is the group size; the segment that corresponds to the root process is not moved.

  - *sendcounts* \[in\]  
    The number of elements to send to each process. If *sendcount\[i\]* is zero, the data part of the message for that process is empty.
    
    The *sendcount* parameter is ignored for all non-root processes.

  - *displs* \[in\]  
    The locations of the data to send to each communicator process. Each location in the array is relative to the corresponding element of the *sendbuf* array.
    
    In the *sendbuf*, *sendcounts*, and *displs* parameter arrays, the *n*th element of each array refers to the data to be sent to the *n*th communicator process.
    
    This parameter is significant only at the root process.

  - *sendtype*  
    The MPI data type of each element in the buffer.
    
    The *sendcount* parameter is ignored for all non-root processes.

  - *recvbuf* \[out\]  
    The pointer to a buffer that contains the data that is received on each process. The number and data type of the elements in the buffer are specified in the *recvcount* and *recvtype* parameters.

  - *recvcount*  
    The number of elements in the receive buffer. If the count is zero, the data part of the message is empty.

  - *recvtype*  
    The data type of the elements in the receive buffer.

  - *root*  
    The rank in the sending process within the specified communicator.

  - *comm*  
    The [**MPI\_Comm**](mpi-comm-enumeration.md) communicator handle.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

``` FORTRAN
    MPI_SCATTERV(SENDBUF, SENDCOUNT, DISPLS, SENDTYPE, RECVBUF, RECVCOUNT, RECVTYPE, ROOT, COMM, IERROR)
        <type> SENDBUF(*), RECVBUF(*)
        INTEGER SENDCOUNT, SENDTYPE, DISPLS(*), RECVCOUNT(*), RECVTYPE, ROOT, COMM, IERROR
```

## Remarks

The **MPI\_Scatterv** function extends the functionality of the [**MPI\_Scatter**](mpi-scatter-function.md) function by allowing a varying count of data, as specified in the *sendcounts* array, to be sent to each process.

The specification of counts, types, and displacements should not cause any location on the root to be read more than one time.

All the function parameters are significant on the root process, only the *recvbuf*, *recvcount*, *recvtype*, *root*, and *comm* parameters are significant on the other processes. The *root* and *comm* parameters must be identical on all processes.

The type signature as specified by the *sendcount*, and *sendtype* parameters for the root process must be equal to the type signature as specified by the *recvcount*, and *recvtype* parameters for all processes. Therefore, the amount of data sent must be equal to the amount of data that is received between any pair of processes. Distinct type maps between sender and receiver are still allowed.

If comm is an intracommunicator, the result is as if the root executed *n* send operations `MPI_Send(sendbuf + displs[i]*extent(sendtype), sendcounts[i], sendtype, I, …)`; and each process executed a receive, `MPI_Recv(recvbuf, recvcount, recvtype, i,…)`.

If the *comm* parameter references an intercommunicator, then the call involves all processes in the intercommunicator, but with one group, group A, that defines the root process. All processes in the other group, group B, set the same value in *root* parameter, that is, the rank of the root process in group A. The root process sets the value **MPI\_ROOT** in the *root* parameter. All other processes in group A set the value **MPI\_PROC\_NULL** in the *root* parameter. Data is broadcast from the root process to all processes in group B. The *buffer* parameters of the processes in group B must be consistent with the *buffer* parameter of the root process.

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

[**MPI\_Gather**](mpi-gather-function.md)

[**MPI\_Gatherv**](mpi-gatherv-function.md)

[**MPI\_Scatter**](mpi-scatter-function.md)

