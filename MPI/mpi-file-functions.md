---
title: MPI File Functions
TOCTitle: MPI File Functions
ms:assetid: 082D0346-E740-491E-B968-7488790EB467
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Dn473310(v=VS.85)
ms:contentKeyID: 59360856
ms.date: 03/28/2018
mtps_version: v=VS.85
---

# MPI File Functions

## In this section

  - [**MPI\_File\_close**](mpi-file-close-function.md)  
    Closes a file.

  - [**MPI\_File\_delete**](mpi-file-delete-function.md)  
    Deletes a file.

  - [**MPI\_File\_get\_amode**](mpi-file-get-amode-function.md)  
    Returns the file access mode.

  - [**MPI\_File\_get\_atomicity**](mpi-file-get-atomicity-function.md)  
    Returns the atomicity mode.

  - [**MPI\_File\_get\_byte\_offset**](mpi-file-get-byte-offset-function.md)  
    Returns the absolute byte position in the file corresponding to "offset" etypes relative to the current view.

  - [**MPI\_File\_get\_group**](mpi-file-get-group-function.md)  
    Returns the group of processes that opened the file.

  - [**MPI\_File\_get\_info**](mpi-file-get-info-function.md)  
    Returns the hints for a file that are actually being used by MPI.

  - [**MPI\_File\_get\_position**](mpi-file-get-position-function.md)  
    Returns the current position of the individual file pointer in etype units relative to the current view.

  - [**MPI\_File\_get\_position\_shared**](mpi-file-get-position-shared-function.md)  
    Returns the current position of the shared file pointer in etype units relative to the current view.

  - [**MPI\_File\_get\_size**](mpi-file-get-size-function.md)  
    Returns the file size.

  - [**MPI\_File\_get\_type\_extent**](mpi-file-get-type-extent-function.md)  
    Returns the extent of datatype in the file.

  - [**MPI\_File\_get\_view**](mpi-file-get-view-function.md)  
    Returns the file view.

  - [**MPI\_File\_iread**](mpi-file-iread-function.md)  
    Nonblocking read using individual file pointer.

  - [**MPI\_File\_iread\_at**](mpi-file-iread-at-function.md)  
    Nonblocking read using explict offset.

  - [**MPI\_File\_iread\_shared**](mpi-file-iread-shared-function.md)  
    Nonblocking read using shared file pointer.

  - [**MPI\_File\_iwrite**](mpi-file-iwrite-function.md)  
    Nonblocking write using individual file pointer.

  - [**MPI\_File\_iwrite\_at**](mpi-file-iwrite-at-function.md)  
    Nonblocking write using explict offset.

  - [**MPI\_File\_iwrite\_shared**](mpi-file-iwrite-shared-function.md)  
    Nonblocking write using shared file pointer.

  - [**MPI\_File\_open**](mpi-file-open-function.md)  
    Opens a file.

  - [**MPI\_File\_preallocate**](mpi-file-preallocate-function.md)  
    Preallocates storage space for a file.

  - [**MPI\_File\_read**](mpi-file-read-function.md)  
    Read using individual file pointer.

  - [**MPI\_File\_read\_all**](mpi-file-read-all-function.md)  
    Collective read using individual file pointer.

  - [**MPI\_File\_read\_all\_begin**](mpi-file-read-all-begin-function.md)  
    Begin a split collective read using individual file pointer.

  - [**MPI\_File\_read\_all\_end**](mpi-file-read-all-end-function.md)  
    Complete a split collective read using individual file pointer.

  - [**MPI\_File\_read\_at**](mpi-file-read-at-function.md)  
    Read using explict offset.

  - [**MPI\_File\_read\_at\_all**](mpi-file-read-at-all-function.md)  
    Collective read using explict offset.

  - [**MPI\_File\_read\_at\_all\_begin**](mpi-file-read-at-all-begin-function.md)  
    Begin a split collective read using explict offset.

  - [**MPI\_File\_read\_at\_all\_end**](mpi-file-read-at-all-end-function.md)  
    Complete a split collective read using explict offset.

  - [**MPI\_File\_read\_ordered**](mpi-file-read-ordered-function.md)  
    Collective read using shared file pointer.

  - [**MPI\_File\_read\_ordered\_begin**](mpi-file-read-ordered-begin-function.md)  
    Begin a split collective read using shared file pointer.

  - [**MPI\_File\_read\_ordered\_end**](mpi-file-read-ordered-end-function.md)  
    Complete a split collective read using shared file pointer.

  - [**MPI\_File\_read\_shared**](mpi-file-read-shared-function.md)  
    Read using shared file pointer.

  - [**MPI\_File\_seek**](mpi-file-seek-function.md)  
    Updates the individual file pointer.

  - [**MPI\_File\_seek\_shared**](mpi-file-seek-shared-function.md)  
    Updates the shared file pointer.

  - [**MPI\_File\_set\_atomicity**](mpi-file-set-atomicity-function.md)  
    Sets the atomicity mode.

  - [**MPI\_File\_set\_info**](mpi-file-set-info-function.md)  
    Sets new values for the hints associated with a file.

  - [**MPI\_File\_set\_size**](mpi-file-set-size-function.md)  
    Sets the file size.

  - [**MPI\_File\_set\_view**](mpi-file-set-view-function.md)  
    Sets the file view.

  - [**MPI\_File\_sync**](mpi-file-sync-function.md)  
    Causes all previous writes to be transferred to the storage device.

  - [**MPI\_File\_write**](mpi-file-write-function.md)  
    Write using individual file pointer.

  - [**MPI\_File\_write\_all**](mpi-file-write-all-function.md)  
    Collective write using individual file pointer.

  - [**MPI\_File\_write\_all\_begin**](mpi-file-write-all-begin-function.md)  
    Begin a split collective write using individual file pointer.

  - [**MPI\_File\_write\_all\_end**](mpi-file-write-all-end-function.md)  
    Complete a split collective write using individual file pointer.

  - [**MPI\_File\_write\_at**](mpi-file-write-at-function.md)  
    Write using explict offset.

  - [**MPI\_File\_write\_at\_all**](mpi-file-write-at-all-function.md)  
    Collective write using explict offset.

  - [**MPI\_File\_write\_at\_all\_begin**](mpi-file-write-at-all-begin-function.md)  
    Begin a split collective write using explict offset.

  - [**MPI\_File\_write\_at\_all\_end**](mpi-file-write-at-all-end-function.md)  
    Complete a split collective write using explict offset.

  - [**MPI\_File\_write\_ordered**](mpi-file-write-ordered-function.md)  
    Collective write using shared file pointer.

  - [**MPI\_File\_write\_ordered\_begin**](mpi-file-write-ordered-begin-function.md)  
    Begin a split collective write using shared file pointer.

  - [**MPI\_File\_write\_ordered\_end**](mpi-file-write-ordered-end-function.md)  
    Complete a split collective write using shared file pointer.

  - [**MPI\_File\_write\_shared**](mpi-file-write-shared-function.md)  
    Write using shared file pointer.

  - [**MPI\_Register\_datarep**](mpi-register-datarep-function.md)  
    Register a set of user-provided data conversion.

  - [*MPI\_Datarep\_conversion\_function*](mpi-datarep-conversion-function-callback-function.md)  
    This function is a place holder for the user-defind functions to converts from file data representation to native representation and vice versa.

  - [*MPI\_Datarep\_extent\_function*](mpi-datarep-extent-function-callback-function.md)  
    This function is a placeholder for user-defined extent callback functions.

