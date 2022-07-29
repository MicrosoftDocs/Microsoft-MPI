---
title: Microsoft MPI Release Notes
TOCTitle: Microsoft MPI Release Notes
ms:assetid: C53BE921-FA3A-49EF-B771-20CAB2FAC955
ms:mtpsurl: https://msdn.microsoft.com/en-us/library/Mt147726(v=VS.85)
ms:contentKeyID: 65803983
ms.date: 03/28/2018
mtps_version: v=VS.85
---

# Microsoft MPI Release Notes

This document contains the release notes for the current versions of Microsoft MPI (MS-MPI) for Windows.

## MS-MPI v10.0 (October 2018)
MS-MPI v10.0 includes the following improvements and fixes. Download MS-MPI v10.0 from the [Microsoft Download Center](https://www.microsoft.com/download/details.aspx?id=57467).

- Support all RMA operations
- Support for utilizing multiple processor groups
- Include IMB-MPI1 and IMB-NBC benchmarks
- Add option in mpiexec/smpd to redirect logs
- Remove nonstandard intrinsics/types to support usage with MinGW/gFortran

- Fix a bug in core dump creation
- Fix a bug in MPI_THREAD_MULTIPLE mode
- Fix a bug in MSMPILaunchSvc that prevents saving credentials

The MS-MPI v10.0 SDK is also available on [nuget](https://www.nuget.org/packages/msmpisdk/).

## MS-MPI v9.0.1 (March 2018)

MS-MPI v9.0.1 includes the following improvements and fixes. Download MS-MPI v9.0.1 from the [Microsoft Download Center](https://go.microsoft.com/fwlink/p/?linkid=389556).

  - Fix for a bug in **mpiexec** code that causes a deadlock during startup on Windows 7 systems.

  - Fix for a bug that prevents **smpd** from spawning processes across all processor groups.

  - Fix for return values for [**MPI\_Win\_Get\_Attr**](mpi-win-get-attr-function.md) for dynamic window.

  - Fix for a bug during named pipe creation in **smpd**.

## MS-MPI v9.0 (February 2018)

MS-MPI v9.0 includes the following new features, improvements, and fixes.

  - Support for **MPI\_Win\_allocate**.

  - Support for **MPI\_Win\_create\_dynamic**, **MPI\_Win\_attach**, and **MPI\_Win\_detach**.

  - Support for **MPI\_Win\_flush**.

  - Support for **MPI\_NO\_OP**.

  - Partial support for **MPI\_Rput**, **MPI\_Rget**, and **MPI\_Raccumulate**.

  - A bug in RMA error reporting.

  - A bug in MS-MPI v7 and v8 that causes deadlock on [**MPI\_Finalize**](mpi-finalize-function.md) in certain conditions.

  - The MS-MPI v9.0 SDK is also available on [nuget.](https://www.nuget.org/packages/msmpisdk/)

## MS-MPI v8.1 (June 2017)

MS-MPI v8.1 includes the following new features, improvements, and fixes.

  - Support for **MPI\_Comm\_spawn** and **MPI\_Comm\_spawn\_multiple**.

  - Support Unicode mpiexec command line arguments and applications command line.

  - Support falling back to NTLM for MS-MPI runtime security requirements.

  - Support multiple processor groups when running smpd daemon or the MS-MPI Launch service.

  - A bug in MS-MPI v8 that might cause crashes due to overflow when using collectives.

  - A bug in MS-MPI v8 that might cause a deadlock in [**MPI\_Alltoallv**](mpi-alltoallv-function.md).

  - A bug in MS-MPI v8 that cause undefined behavior when dealing with large files.

  - The MS-MPI v8.1 SDK is also available on [nuget.](https://www.nuget.org/packages/msmpisdk/)

## MS-MPI v8 (January 2017)

MS-MPI v8 includes the following new features, improvements, and fixes.

  - Complete support for all non-blocking collectives.

  - Support for **MPI\_Reduce\_scatter\_block**.

  - Performance improvement for [**MPI\_Alltoallv**](mpi-alltoallv-function.md) and [**MPI\_Alltoallw**](mpi-alltoallw-function.md).

  - A bug in MS-MPI v7 that causes missing information in the event source for the MSMPI Launch Service

  - A bug in MS-MPI v7.1 that causes a hang in MSMPI Launch Service.

  - A bug in MS-MPI v7 that can results in a bad port string returned from [**MPI\_Open\_port**](mpi-open-port-function.md).

  - The MS-MPI v8 SDK is also available on [nuget.](https://www.nuget.org/packages/msmpisdk/)

## MS-MPI v7.1 (June 2016)

MS-MPI v7.1 includes the following notable improvements and fixes to MS-MPI v7.

  - Setup is now more resilient and will not fail when previous uninstallations did not successfully clean up the Registry.

  - A bug in MS-MPI v7 is fixed that causes jobs to fail when a large number of MPI jobs are executed concurrently on the same set of nodes.

  - Authentication automatically falls back to NTLM if Kerberos authentication fails in an environment with partial or misconfigured Kerberos support.

  - mpiexec supports Unicode characters in the command line and no longer has a hard-coded limit for command line length. Long path notation (\\\\?\\) is also supported.

  - The MS-MPI v7.1 SDK is also available on [nuget.](https://www.nuget.org/packages/msmpisdk/)

## MS-MPI v7 (November 2015)

MS-MPI v7 is the successor to the MS-MPI v6. Download MS-MPI v7 from the [Microsoft Download Center](https://www.microsoft.com/download/details.aspx?id=49926).

### New features

MS-MPI v7 includes the following new features, improvements, and fixes.

  - **Support for additional non-blocking collective operations**: [**MPI\_Iallreduce**](mpi-iallreduce-function.md), [**MPI\_Iscatter**](mpi-iscatter-function.md), [**MPI\_Iallgather**](mpi-iallgather-function.md), [**MPI\_Iscatterv**](mpi-iscatterv-function.md), and [**MPI\_Igatherv**](mpi-igatherv-function.md). These are in addition to the already supported [**MPI\_Ibcast**](mpi-ibcast-function.md), [**MPI\_Ireduce**](mpi-ireduce-function.md), [**MPI\_Igather**](mpi-igather-function.md) and [**MPI\_Ibarrier**](mpi-ibarrier-function.md).

  - **Support for configuring the port range for Network Direct connections** by using the **MSMPI\_ND\_PORT\_RANGE** environment variable

  - **Revamped process management** (mpiexec/smpd) for better reliability and performance

  - **Performance improvements** for collective operations

  - **MPI launch service** - MS-MPI v7 introduces the MS-MPI launch service, which allows the launching of MPI processes for local and remote machines with user-provided credentials. The MS-MPI redistributable package installs the MS-MPI launch service in Manual mode. To start the service, run the following command:
    
    `sc start MSMPILaunchSvc [options]`
    
    These are the options you can pass to the launch service at service start:
    
      - *-p | -port \<port\>* - Change the port that launch service is listening on.
    
      - *-g | -group \<group name\>* - Only allow members of the specified group to run MPI applications. If not specified, the default is authenticated users.

  - **New mpiexec options for launch service** - There are two new options to mpiexec (*-pwd* and *-savecreds*) that allow you to provide the necessary credentials for launching processes using the launch service. The *-pwd* option allows specifying the password for the submitting users in non-interactive scenarios (e.g., using a script or scheduled task). In this case the password is provided in clear text. The *-savecreds* option causes the provided credentials (if specified with *-pwd*) to be securely stored on all the hosts specified in the mpiexec command line.
    
    For example, the following command will prompt for the user's password and ask the user if he or she wants to store it on the specified machines *host1* and *host2*, then launch three processes, one on *host1* and two on *host2*:
    
    `mpiexec –hosts 2 host1 1 host2 2 –wdir C:\MpiTests mpiapp.exe [parameters]`
    
    As another example, the following command will authenticate the user using the provided password, store it on the specified machines *host1* and *host2*, then launch three processes, one on *host1* and two on *host2*:
    
    `mpiexec –hosts 2 host1 1 host2 2 –wdir C:\MpiTests -pwd <password> -savecreds mpiapp.exe [parameters]`
    
    After you run mpiexec with the *-savecreds* option on a set of nodes, you do not have to provide the password on subsequent runs for those nodes unless the password is changed. If the user is running in interactive mode, mpiexec prompts for the password if the launch service is running and the password has not been provided or previously saved with the *-savecreds* option.

###  HPC Pack compatibility

MS-MPI v7 is compatible with HPC Pack 2012 R2 and later. If you are running a compatible version of HPC Pack that has an earlier version of MS-MPI, you can upgrade MS-MPI to v7.

## MS-MPI v6 (May 2015)

MS-MPI v6 is the successor to the MS-MPI v5 redistributable package (released in November 2014). Download MS-MPI v6 from the Microsoft Download Center.

### New features

MS-MPI v6 includes the following new features, improvements, and fixes.

  - **Non-blocking collective operations** including [**MPI\_Ibcast**](mpi-ibcast-function.md), [**MPI\_Ireduce**](mpi-ireduce-function.md), [**MPI\_Igather**](mpi-igather-function.md) and [**MPI\_Ibarrier**](mpi-ibarrier-function.md).

  - **Multi-job affinity support** so that multiple affinitized MPI jobs can co-exist on a single machine without overlapping the cores they run on. The MPI runtime now detects that there are existing jobs pinned to cores, and will launch subsequent jobs on cores that are not currently in use.
    
    The feature is exposed as a new option to [mpiexec](https://technet.microsoft.com/en-us/library/cc947675.aspx) (*-affinity\_auto* or *–aa*) and is designed to work both under job schedulers such as Microsoft HPC Pack and in standalone SDK mode.
    
    As an example, to run two 8 core jobs on a single 16 core machine you could use the following command line:
    
    `mpiexec –cores 8 –affinity_auto –affinity_layout sequential myapp.exe`, or
    
    `mpiexec –c 8 –aa –al seq myapp.exe`

  - **Support for multi-threaded applications** by enabling the use of **MPI\_THREAD\_MULTIPLE** when calling [**MPI\_Init\_thread**](mpi-init-thread-function.md). This is designed to allow hybrid applications using OMP or other threading models to more easily leverage the MPI runtime.
    
    The minimum supported server for this feature is Windows Server 2012. The minimum supported client for this feature is Windows 8.

  - **New features from the** [MPI 3.0 standard](https://www.mpi-forum.org/docs/mpi-3.0/mpi30-report.pdf) including:
    
      - Support for [**MPI\_Mprobe**](mpi-mprobe-function.md), [**MPI\_Mrecv**](mpi-mrecv-function.md), [**MPI\_Improbe**](mpi-improbe-function.md), and [**MPI\_Imrecv**](mpi-imrecv-function.md)
      - Support for **MPI\_COUNT**, to allow large datatypes to be properly represented in [**MPI\_STATUS**](mpi-status-structure.md) structures
      - Support for [**MPI\_Type\_create\_hindexed\_block**](mpi-type-create-hindexed-block-function.md)
      - Support for [**MPI\_Dist\_graph\_create**](mpi-dist-graph-create-function.md), [**MPI\_Dist\_graph\_create\_adjacent**](mpi-dist-graph-create-adjacent-function.md), [**MPI\_Dist\_graph\_neighbors**](mpi-dist-graph-neighbors-function.md), and [**MPI\_Dist\_graph\_neighbors\_count**](mpi-dist-graph-neighbors-count-function.md)

###  HPC Pack compatibility

MS-MPI v6 is compatible with HPC Pack 2012 R2 and later. If you are running a compatible version of HPC Pack that has an earlier version of MS-MPI, you can upgrade MS-MPI to v6.

###  Changes to default settings

MS-MPI v6 changes the following [mpiexec](https://technet.microsoft.com/en-us/library/cc947675.aspx) default settings:

  - MSMPI\_ND\_ZCOPY\_THRESHOLD is set to -1, disabling zcopy. This can be reenabled by setting MSMPI\_ND\_ZCOPY\_THRESHOLD=0 in the mpiexec command line, or via [cluscfg setenvs](https://technet.microsoft.com/library/cc972901.aspx) (if you are using Microsoft HPC Pack).
  - MSMPI\_HA\_COLLECTIVE is set to all, enabling hierarchical collectives by default. This can be disabled by setting MSMPI\_HA\_COLLECTIVE=off, again through the mpiexec command line or externally.

### Deprecated features

We are deprecating the built in auto-tuning functionality in this version with the intention of moving the auto-tuner into a separate utility in an upcoming release.

##  Community resources

  - [Windows HPC MPI Forum](https://social.microsoft.com/forums/en-us/home?forum=windowshpcmpi)
  - [Contact the MS-MPI Team](mailto:askmpi@microsoft.com)

## Related topics

[Microsoft MPI](microsoft-mpi.md)

[MPI Reference](mpi-reference.md)

