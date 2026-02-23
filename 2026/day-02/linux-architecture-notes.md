- The core components of Linux (kernel, user space, init/systemd)

    1. **Kernel**:
        My understanding: Kernel is the core of a OS. It is them set of programs which interact directly with hardware, acts like mediator between the high level software and hardware.
        It manages system resources  - CPU , memory and devices
        It handles running program, accessing files and connecting IO devices
        Facilitates comm b/.w hardware and user appl
        Ensure efficient and secure multitasking
        Manages system stability and prevents unauthorized resource access

        Functions of Kernel
        Process Management : Scheduling and execution of processes.
        Memory Management : Allocation and deallocation of memory space, managing virtual memory, handling memory protection and sharing.
        Device Management : Managing input/output devices, providing a unified interface for hardware devices and handling device driver communication.
        File System Management : Managing file operations and providing a file system interface to applications.
        Resource Management : Managing system resources (CPU time, disk space, network bandwidth). Mainly allocating and deallocating resources as needed.
        Security and Access Control : Enforcing access control policies like user permissions and authentication.
        Inter-Process Communication : Facilitating communication between processes by providing mechanisms like message passing and shared memory.
       
        Types of Kernel
        The following are different types of kernels.
        Monolithic kernel: all OS services run in kernel space → fast, but less fault-isolation. Examples are Unix, Linux, Open VMS, XTS-400 etc.
        Microkernel: minimal kernel functionality; most services moved to user space → better reliability, but more overhead. Examples are Minix 3 and Mach (true microkernel versions like Mach 3.0),
        Hybrid kernel: mixes monolithic + microkernel ideas; some services in kernel for speed, others isolated for safety. Examples are Windows NT family (Windows 2000, XP, Vista, 7, 8, 10 etc.), macOS / XNU, ReactOS and Haiku OS
        Nanokernel: extremely minimal kernel, providing only basic hardware abstraction; everything else outside. Examples are Nemesis and MIT Exokernel projects like XOK, Aegis
        Exokernel: separates protection vs. management; gives apps direct control over hardware abstractions so apps decide what abstractions to build.

    2. **User space** :
        A user space process is executed by a user in the operating system, rather than being part of the operating system itself. It might also be executed by an init system (e.g. systemd), but it isn't part of the kernel. User space is the area of memory that non-kernel applications run in. User space processes literally run in the user space part of memory. A user space process runs in user mode, which is the non-privileged execution mode that the process' instructions are executed with. User mode processes have to switch to kernel mode when they want to consume services provided by the kernel (e.g. disk I/O, network access). Switching to kernel mode involves triggering a syscall to be executed by the kernel. This mechanism is described in bit more detail below.

        User mode execution of user-run processes ensures that a user space process cannot access or modify memory managed by the kernel, and can't interfere with another process' execution. This is an important security control in ensuring that user-run processes cannot corrupt or interfere with the operating system.

    3. **init / systemd**
        - Process ID: 1
        init: SysVinit system - init process
        - First process
        - Responsible to bringing up the system to usuable state by starting the system processes.  RUNNING STARTUP PROCESSES AND MANAGING RUNLEVELS
            - Startup processes based on    
                                        config files: '/etc/inittab'
                                        scripts : 'etc/rc.d'
            - These are executed sequentially acc to RUNLEVEL
                                                        RUNLEVEL: 
                                                            0- Halt teh sys
                                                            1- Single user mode
                                                            3- Multi user mode without graphical interface
                                                            5- Multi user mode with graphical interface
                                                            6- Reboot the sys

        **systemd: system and service manager**
        - it replaced traditional init to overcome the limitation of init
        - it is unit based : each service, scekt device or mount point is representd as unit file. stored in  "/usr/lib/systemd/system/"  "/etc/systemd/system"
        - better than init :               
                        paralles serive startup,  
                        on demand service activation, 
                        Socket and D-BUS activation - serives start on events, 
                        integrated logging "journalctl".
                        target units - grouping of serives and controlling the systems state
        
    4.  **How processes are created and managed**
        - a process is running instance of program
        - a process creates another process or events- parent process --> child process .
        - unique identification via PID assigned by kernel
        - Process Creation: fork() and exec()
        -  Process Control Block (PCB) is a data structure used by the operating system to store all relevant information about a process. 
        -  Process Scheduler - determines which process gets to execute and for how long
        - Commands :
            ps
            top
            htop
            kill  
            nice    

    5. **What systemd does and why it matters**
        - system and service manager. PID -1
        - is started just after kernel is loaded BIOS-> Kernel -> Systemd
        - booting pc, starting and stoping serives, managing services, managing processes and handling system shutdowns

    6.  **List of 5 commands used daily**
        - ls
        - cat
        - cd
        - mkdir
        - touch
        - pwd