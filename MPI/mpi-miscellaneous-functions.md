---
title: MPI Miscellaneous Functions
TOCTitle: MPI Miscellaneous Functions
ms:assetid: 707D73BB-2AC4-4A56-9CFC-3B328E21567D
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473434(v=VS.85)
ms:contentKeyID: 59360970
ms.date: 03/28/2018
mtps_version: v=VS.85
---

# MPI Miscellaneous Functions

## In this section

  - [**MPI\_Address**](mpi-address-function.md)  
    This function is deprecated in MPI-2 and removed from MPI-3. It is replaced by the [**MPI\_Get\_address**](mpi-get-address-function.md) function.

  - [**MPI\_Attr\_delete**](mpi-attr-delete-function.md)  
    This function is deprecated in MPI-2 and removed from MPI-3. It is replaced by the [**MPI\_Comm\_delete\_attr**](mpi-comm-delete-attr-function.md) function.

  - [**MPI\_Attr\_get**](mpi-attr-get-function.md)  
    This function is deprecated in MPI-2 and removed from MPI-3. It is replaced by the [**MPI\_Comm\_get\_attr**](mpi-comm-get-attr-function.md) function.

  - [**MPI\_Attr\_put**](mpi-attr-put-function.md)  
    This function is deprecated in MPI-2 and removed from MPI-3. It is replaced by the [**MPI\_Comm\_set\_attr**](mpi-comm-set-attr-function.md) function.

  - [**MPI\_Buffer\_attach**](mpi-buffer-attach-function.md)  
    [**MPI\_Buffer\_detach**](mpi-buffer-detach-function.md)  
    Attaches / removes a user-provided buffer for sending.

  - [**MPI\_Comm\_get\_name**](mpi-comm-get-name-function.md)  
    Returns the print name from the communicator.

  - [**MPI\_Comm\_set\_name**](mpi-comm-set-name-function.md)  
    Sets the print name for a communicator.

  - [**MPI\_File\_c2f**](mpi-file-c2f-function.md)  
    Translates a C file handle to a Fortran file handle.

  - [**MPI\_File\_f2c**](mpi-file-f2c-function.md)  
    Translates a Fortran file handle to a C file handle.

  - [**MPI\_Keyval\_create**](mpi-keyval-create-function.md)  
    This function is deprecated in MPI-2 and removed from MPI-3. It is replaced by the [**MPI\_Comm\_create\_keyval**](mpi-comm-create-keyval-function.md) function.

  - [**MPI\_Keyval\_free**](mpi-keyval-free-function.md)  
    This function is deprecated in MPI-2 and removed from MPI-3. It is replaced by the [**MPI\_Comm\_free\_keyval**](mpi-comm-free-keyval-function.md) function.

  - [**MPI\_Pcontrol**](mpi-pcontrol-function.md)  
    Controls profiling.

  - [**MPI\_Status\_c2f**](mpi-status-c2f-function.md)  
    Converts from a C status (which is a structure) to a Fortran status (which is an array of integers).

  - [**MPI\_Status\_f2c**](mpi-status-f2c-function.md)  
    Converts from a Fortran status (which is an array of integers) to a C status (which is a structure).

  - [**MPI\_Type\_create\_f90\_complex**](mpi-type-create-f90-complex-function.md)
  
    [**MPI\_Type\_create\_f90\_integer**](mpi-type-create-f90-integer-function.md)
    
    [**MPI\_Type\_create\_f90\_real**](mpi-type-create-f90-real-function.md)  
    Returns a predefined type that matches the specified range.

  - [**MPI\_Type\_extent**](mpi-type-extent-function.md)  
    This function is deprecated in MPI-2 and removed from MPI-3. It is replaced by the [**MPI\_Type\_get\_extent**](mpi-type-get-extent-function.md) function.

  - [**MPI\_Type\_get\_name**](mpi-type-get-name-function.md)  
    Gets the print name for a datatype.

  - [**MPI\_Type\_hindexed**](mpi-type-hindexed-function.md)  
    This function is deprecated in MPI-2 and removed from MPI-3. It is replaced by the [**MPI\_Type\_create\_hindexed**](mpi-type-create-hindexed-function.md) function.

  - [**MPI\_Type\_hvector**](mpi-type-hvector-function.md)  
    This function is deprecated in MPI-2 and removed from MPI-3. It is replaced by the [**MPI\_Type\_create\_hvector**](mpi-type-create-hvector-function.md) function.

  - [**MPI\_Type\_lb**](mpi-type-lb-function.md)  
    This function is deprecated in MPI-2 and removed from MPI-3. It is replaced by the [**MPI\_Type\_get\_extent**](mpi-type-get-extent-function.md) function.

  - [**MPI\_Type\_match\_size**](mpi-type-match-size-function.md)  
    Finds an MPI datatype matching a specified size.

  - [**MPI\_Type\_set\_name**](mpi-type-set-name-function.md)  
    Sets a name for a datatype.

  - [**MPI\_Type\_struct**](mpi-type-struct-function.md)  
    This function is deprecated in MPI-2 and removed from MPI-3. It is replaced by the [**MPI\_Type\_create\_struct**](mpi-type-create-struct-function.md) function.

  - [**MPI\_Type\_ub**](mpi-type-ub-function.md)  
    This function is deprecated in MPI-2 and removed from MPI-3. It is replaced by the [**MPI\_Type\_get\_extent**](mpi-type-get-extent-function.md) function.

  - [**MPI\_Win\_get\_name**](mpi-win-get-name-function.md)  
    Gets the print name associated with the MPI window object.

  - [**MPI\_Win\_set\_name**](mpi-win-set-name-function.md)  
    Sets the print name for an MPI window object.

  - [**MPIR\_Dup\_fn**](mpir-dup-fn-function.md)  
    A function to copy attributes.

  - [**MSMPI\_Get\_bsend\_overhead**](msmpi-get-bsend-overhead-function.md)  
    Returns the size of the overhead required for Bsend buffers.

  - [**MSMPI\_Get\_version**](msmpi-get-version-function.md)  
    Returns the version number of the MSMPI feature set.

  - [**MSMPI\_Request\_set\_apc**](msmpi-request-set-apc-function.md)  
    Sets an APC callback to be invoked on the calling thread when the request completes.

