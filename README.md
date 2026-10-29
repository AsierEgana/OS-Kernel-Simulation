# Operating System Kernel Simulation

A basic operating system simulation implemented in C as part of an Operating Systems course project. The program models process scheduling, timer ticks, process execution and multiple CPU execution threads.

## Features

- **Process generation:** Creates processes with randomly assigned execution times and priorities.
- **Process scheduling:** Implements three scheduling policies:
  - **First-Come, First-Served (FCFS):** Assigns ready processes to available execution threads.
  - **Round Robin (RR):** Uses a time quantum to manage process execution and reschedule unfinished processes.
  - **Priority-based Round Robin:** Combines Round Robin scheduling with process priorities and priority degradation after a time quantum expires.
- **Multithreading:** Uses POSIX threads (`pthreads`) to manage the clock, timer, process generator and scheduler.
- **Configurable execution:** Allows the user to specify clock frequency, process generation interval, scheduler interval, number of CPUs, cores and threads.
- **Execution monitoring:** Displays timer ticks, process creation, scheduling decisions and process completion in the terminal.

## Technologies

- C
- POSIX Threads (`pthreads`)
- Linux/Unix system programming

## Compilation

Compile the source file using GCC:

```bash
gcc kernel.c -o kernel -pthread
```

## Usage

Run the executable with six numerical arguments:

```bash
./kernel <tick_frequency> <process_generation_interval> <scheduler_interval> <cpu_count> <core_count> <thread_count>
```

### Example

```bash
./kernel 4 2 2 1 2 3
```

This example configures a clock frequency of 4 ticks per second, process generation and scheduling intervals of 2 seconds, and a simulated configuration of 1 CPU, 2 cores and 3 threads per core.

After starting the program, select one of the available scheduling policies:

1. FCFS
2. Round Robin
3. Round Robin with priority degradation

The program then generates processes and displays scheduling activity in the terminal.

## Learning Objectives

This project explores fundamental operating system concepts, including process control blocks, ready queues, CPU scheduling, time quantum management, thread synchronization and concurrent programming in C.

## Project Context

Developed as part of a university Operating Systems course, with the objective of implementing a simplified model of an operating system's process scheduling mechanisms.
