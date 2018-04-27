##1. List all of the main states a process may be in at any point in time on a standard Unix system. Briefly explain what each of these states mean.
There are 5 main states that a process may be in any point in time,t
Created: Upon initiation of a process, but not allocated cpu time by scheduler yet.
Ready: Waiting to be run by CPU.
Running: Executed by CPU
Blocked: Currently a running process but interrupted/stopped by something and needs to be unblocked to continue.
Terminated: Ended execution. However still in the process table until exited.
##2. What is a Zombie Process? How does it get created? How does it get destroyed?
A zombie process that has already actually been terminated. It gets destroyed by receiving an 'exit' call.
##3. Describe the job of the Scheduler in the OS in general.
The job of the scheduler is to determine how much time to allocate from the cpu to each process to do work on. It decides this by placing priority levels for each process. Processes that are fast to finish and high priority are 1st, followed by low priority fast finishing processes, high priority slow finishing, and finally low priority slow finishing processes.
##4. Describe the benefits of the MLFQ over a plain Round-Robin scheduler.
Round Robin is a more 'fair' scheduler over MLFQ as it plainly time-slices all processes with no priority levels. Whereas MLFQ tries to determine which processes are higher priority and therefore can allocate more cpu time to more operational important processes such as mouse movement or foreground applications. This way the user may experience a greater sense of responsiveness. 