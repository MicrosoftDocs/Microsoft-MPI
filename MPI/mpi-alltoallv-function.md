---
title: MPI_Alltoallv function
TOCTitle: MPI_Alltoallv function
ms:assetid: 14a47f9e-b476-4397-9b70-d8d2428b33bd
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473231(v=VS.85)
ms:contentKeyID: 59360777
ms.date: 03/28/2018
mtps_version: v=VS.85
f1_keywords:
- MPI_ALLTOALLV
- mpif/MPI_Alltoallv
- mpi/MPI_ALLTOALLV
dev_langs:
- C++
- C
api_location:
- Msmpi.dll
api_name:
- MPI_Alltoallv
api_type:
- DLLExport
product:
- Windows
topic_type:
- apiref
- kbSyntax
product_family_name: VS
ROBOTS: INDEX,FOLLOW
description: Learn how to use the MPI_Alltoallv function for data gathering and scattering across a group. Understand syntax, parameters, and return values.
---

# MPI\_Alltoallv function

Gathers data from and scatters data to all members of a group. The **MPI\_Alltoallv** function adds flexibility to the [**MPI\_Alltoall**](mpi-alltoall-function.md) function by allowing a varying count of data from each process.

## Syntax

``` c++
int MPIAPI MPI_Alltoallv(
  _In_  void         *sendbuf,
  _In_  int          *sendcounts,
  _In_  int          *sdispls,
        MPI_Datatype sendtype,
  _Out_ void         *recvbuf,
  _In_  int          *recvcounts,
  _In_  int          *rdispls,
        MPI_Datatype recvtype,
        MPI_Comm     comm
);
```

## Parameters

  - *sendbuf* \[in\]  
    The pointer to the data to be sent to all processes in the group. The number and data type of the elements in the buffer are specified in the *sendcount* and *sendtype* parameters. Each element in the buffer corresponds to a process in the group.
    
    If the comm parameter references an intracommunicator, you can specify an in-place option by specifying **MPI\_IN\_PLACE** in all processes. The *sendcount*, *sdispls* and *sendtype* parameters are ignored. Each process enters data in the corresponding receive buffer element.
    
    Data that are sent and received must have the same type map as specified by the *recvcounts* array and the *recvtype* parameter. Data is read from the locations of the receive buffer that is specified by the *rdispls* parameter.

  - *sendcounts* \[in\]  
    The number of data elements that this process sends in the buffer that is specified in the *sendbuf* parameter. If an element in*sendcount* is zero, the data part of the message from that process is empty.

  - *sdispls* \[in\]  
    The location, relative to the *sendbuf* parameter, of the data for each communicator process.
    
    Entry *j* specifies the displacement relative to the *sendbuf* parameter from which to take the outgoing data that is destined for process *j*.

  - *sendtype*  
    The MPI data type of the elements in the send buffer.

  - *recvbuf* \[out\]  
    The pointer to a buffer that contains the data that are received from each process. The number and data type of the elements in the buffer are specified in the *recvcount* and *recvtype* parameters.

  - *recvcounts* \[in\]  
    The number of data elements from each communicator process in the receive buffer.

  - *rdispls* \[in\]  
    The location, relative to the *recvbuf* parameter, of the data from each communicator process.
    
    In the *recvbuf*, *recvcounts*, and *rdispls* parameter arrays, the *n*th element of each array refers to the data that is received from the *n*th communicator process.

  - *recvtype*  
    The MPI data type of each element in buffer.

  - *comm*  
    Specifies the [**MPI\_Comm**](mpi-comm-enumeration.md) communicator handle.

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

``` FORTRAN
    MPI_ALLTOALL(SENDBUF, SENDCOUNT, SENDTYPE, RECVBUF, RECVCOUNT, RECVTYPE,
                COMM, IERROR)
        <type> SENDBUF(*), R.ECVBUF(*)
        INTEGER SENDCOUNT, SENDTYPE, RECVCOUNT, RECVTYPE, COMM, IERROR
```

## Remarks

The type signature that is specified by the *sendcount*, and *sendtype* parameters for a process must be equal to the type signature that is specified by the *recvcount*, and *recvtype* parameters of the receiving process. Therefore, the amount of data sent must be equal to the amount of data that is received between any pair of processes. Distinct type maps between sender and receiver are still allowed.

All parameters are significant on all processes. The *comm* parameter must be identical on all processes.

If the *comm* parameter references an intracommunicator, then the *j*th block that is sent from process *i* is received by process *j* and is placed in the *i*th block of the receive buffer. These blocks do not have to all have the same size.

The outcome of calling the **MPI\_Alltoallv** function is as if each process sent a message to every other process with, `MPI_Send(sendbuf + sdispls[i]*extent(sendtype), sendcounts[i], sendtype, I, …)`, and received a message from every other process with a call to `MPI_Recv(recvbuf + rdispls[i]*extent(recvtype), recvcounts[i], recvtype, I, …)`.

Specifying the in-place option indicates that the same amount and type of data is sent and received between any two processes in the group of the communicator. Different pairs of processes can exchange different amounts of data. Users must ensure that *recvcounts\[j\]* and *recvtype* on process *i* match *recvcounts\[i\]* and *recvtype* on process *j*. This symmetric exchange can be useful in applications where the data to be sent is not be used by the sending process after the **MPI\_Alltoallv** function call.

If the *comm* parameter references an intercommunicator, then the outcome is as if each process in group A sends a message to each process in group B, and vice versa. The *j*th send buffer of process *i* in group A should be consistent with the *i*th receive buffer of process *j* in group B, and vice versa.

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

[MPI Collective Functions](mpi-collective-functions.md)

[**MPI\_Datatype**](mpi-datatype-enumeration.md)

[**MPI\_Alltoall**](mpi-alltoall-function.md)

[**MPI\_Gather**](mpi-gather-function.md)

[**MPI\_Scatter**](mpi-scatter-function.md)

[**MPI\_Send**](mpi-send-function.md)

[**MPI\_Recv**](mpi-recv-function.md)

