---
title: MPI Datatype Functions
TOCTitle: MPI Datatype Functions
ms:assetid: 1B53E575-4B69-4099-AB2E-4007DCB68308
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473291(v=VS.85)
ms:contentKeyID: 59360837
ms.date: 03/28/2018
mtps_version: v=VS.85
---

# MPI Datatype Functions

## In this section

  - [**MPI\_Get\_address**](mpi-get-address-function.md)  
    Gets the address of a location in memory.

  - [**MPI\_Get\_elements**](mpi-get-elements-function.md)  
    Returns the number of basic elements in a datatype.

  - [**MPI\_Pack**](mpi-pack-function.md)  
    Packs a datatype into contiguous memory.

  - [**MPI\_Pack\_external**](mpi-pack-external-function.md)  
    Packs a datatype into contiguous memory, using the external32 format.

  - [**MPI\_Pack\_external\_size**](mpi-pack-external-size-function.md)  
    Returns the upper bound on the amount of space needed to pack a message using [**MPI\_Pack\_external**](mpi-pack-external-function.md).

  - [**MPI\_Pack\_size**](mpi-pack-size-function.md)  
    Returns the upper bound on the amount of space needed to pack a message.

  - [**MPI\_Type\_commit**](mpi-type-commit-function.md)  
    Commits the datatype.

  - [**MPI\_Type\_contiguous**](mpi-type-contiguous-function.md)  
    Defines a new data type that is a concatenation of a number of elements of an existing data type.

  - [**MPI\_Type\_create\_darray**](mpi-type-create-darray-function.md)  
    Creates a datatype representing a distributed array.

  - [**MPI\_Type\_create\_hindexed**](mpi-type-create-hindexed-function.md)  
    Defines a new data type that consists of a specified number of blocks of arbitrary size.

  - [**MPI\_Type\_create\_hindexed\_block**](mpi-type-create-hindexed-block-function.md)  
    Allows replication of an old datatype into a sequence of blocks (each block is a concatenation of the old datatype), where all blocks have the same block length but can have different block displacements in bytes.

  - [**MPI\_Type\_create\_hvector**](mpi-type-create-hvector-function.md)  
    Defines a new data type that consists of a specified number of blocks. Each block is a concatenation of the same number of elements of an existing data type.

  - [**MPI\_Type\_create\_indexed\_block**](mpi-type-create-indexed-block-function.md)  
    Defines a new data type that consists of a specified number of blocks. Each block is the same block length, but each block can have a different block displacement.

  - [**MPI\_Type\_create\_resized**](mpi-type-create-resized-function.md)  
    Creates a datatype with a new lower bound and extent from an existing datatype.

  - [**MPI\_Type\_create\_struct**](mpi-type-create-struct-function.md)  
    Defines a new data type with a specified data type, displacement, and size for each block of data.

  - [**MPI\_Type\_create\_subarray**](mpi-type-create-subarray-function.md)  
    Defines a new data type that consists of an n-dimensional subarray of an n-dimensional array.

  - [**MPI\_Type\_dup**](mpi-type-dup-function.md)  
    Duplicates a datatype.

  - [**MPI\_Type\_free**](mpi-type-free-function.md)  
    Frees the datatype.

  - [**MPI\_Type\_get\_contents**](mpi-type-get-contents-function.md)  
    Gets the type contents.

  - [**MPI\_Type\_get\_envelope**](mpi-type-get-envelope-function.md)  
    Gets the type envelope.

  - [**MPI\_Type\_get\_extent**](mpi-type-get-extent-function.md)  
    Gets the lower bound and extent for a datatype.

  - [**MPI\_Type\_get\_true\_extent**](mpi-type-get-true-extent-function.md)  
    Gets the true lower bound and extent for a datatype.

  - [**MPI\_Type\_indexed**](mpi-type-indexed-function.md)  
    Defines a new data type that consists of a specified number of blocks of arbitrary size.

  - [**MPI\_Type\_size**](mpi-type-size-function.md)  
    Returns the number of bytes occupied by entries in the datatype.

  - [**MPI\_Type\_vector**](mpi-type-vector-function.md)  
    Defines a new data type that consists of a specified number of blocks of a specified size.

  - [**MPI\_Unpack**](mpi-unpack-function.md)  
    Unpacks a buffer according to a datatype into contiguous memory.

  - [**MPI\_Unpack\_external**](mpi-unpack-external-function.md)  
    Unpacks a buffer (packed with [**MPI\_Pack\_external**](mpi-pack-external-function.md)) according to a datatype into contiguous memory.

