---
id: 1fm2gs46y0osv3mdw6i29s7
title: Operating Systems
desc: ''
updated: 1698861822800
created: 1695822906139
---

## [Notes by Nick](https://drive.google.com/drive/folders/1r-DAloIEUxUtUwhT2nqilD_d7oQlj1VQ)

## Week 0
[Introduction PDF](/Operating%20Systems/Week%200%20-%20Introduction.pdf)

All questions on the quizzes are from the lecture slides.

## Week 1
[OS Introduction PDF](/Operating%20Systems/Week%201%20-%20OS%20Introduction.pdf)

[Java Basics Labs PDF](/Operating%20Systems/Week%201%20-%20Java%20.pdf)

(QUIZ)
usermode
kernelmode

CPU - brain of computer is built♠️ of CU(Program counter), ALU(Arithmetic logic unit), registers(small,fast memory) (i think in QUIZ)

Main registers: (couple of questions in QUIZ)
EAX, EBX, ECX, EDX and EBP, ESI, EDI, ESP

(in QUIZ what is output of assembly code 2 questions) 

Interrupts

## Week 2

[Concurrency PDF](/Operating%20Systems/Week%202%20-%20Concurrency.pdf)

[Objects and fields in Java PDF](/Operating%20Systems/Week%202%20-%20Java%20Object%20and%20Fields.pdf)

**Sequential system** 0 computation are executed one after the other

**Concurrent system** -two or more computations are executing at the same time

**Thread** is a sequence of instruction defined by program
Process has one or more threads. Every process has at least one control flow within a single address space.
A process have multiple control flows.

**Parallelism** - Multi-core processors and run threads truly parallel (different threads on different cores).

**Multitasking** - Multiple different threads running on same core 

(QUIZ question about crating java thread nad class extending thread)

When 2 threads run at the same time and and variables are different the result order will be random. we call that **non-deterministic** (or **interference** or **race conditions**).  
If Both threads have same variable for example program counter then we have a problem.

**Critical section** - sections of code that **CANT** overlap OR Set of steps that must be executed to update a shared data structure.
You could avoid interference buy never using same variable names between threads but thats no good.  
or scheduling but that is too restrictive.  

**Race conditions** -  when 2 threads are trying to access same variable at the same time.


## Week 3

[Manual Exclusion PDF](/Operating%20Systems/Week%203%20-%20Mutual%20Exclusion.pdf)

[Threads and Race Conditions](/Operating%20Systems/Week%203%20-%20Threads%20and%20Race%20Conditions.pdf)

**Mutual Exclusion (mutex)** - method that ensures only one thread does particular activity such as executing critical section.

LOCK SCENARIO - does not guarantee safety (IN QUIZ)

IN TURNS SCENARIO - do guarantee safety but not progress

INTEREST SCENARIO - same problem as lock scenario 

Peterson's algorithm - interest and turn at the same time solves the problem but only when there are 2 threads

3 WORKING SOLUTIONS: 
* TSL (hardware) - test and set lock
* Semaphore - integer variable that increases and decreases when threads enter and leave critical section 
* Java synchronization

## Week 4

[Synchronization PDF](/Operating%20Systems/Week%204%20-%20Synchronization.pdf)

[Mutual Exclusion Labs](/Operating%20Systems/Week%204%20-%20Mutual%20exclusion.pdf)

[Notification and Monitors Appendix](/Operating%20Systems/Week%204%20-%20Notification%20and%20Monitors%20Appendix.pdf)

**Deadlock** - when 2 or more threads are waiting for each other to finish and none of them can finish.

Deadlock recovery - kill one of the threads

Avoiding deadlocks 
(SLIDE 23/32 AND LATER ON QUIZ AND EXAM) 

**Unsafe area** - when 2 threads are in critical section at the same time

## Week 5

[Processes and Scheduling PDF](/Operating%20Systems/Week%205%20-%20Processes%20and%20Scheduling.pdf)

[Deadlock Labs](/Operating%20Systems/Week%205%20-%20Deadlock%20Labs.pdf)

**Process** - program in execution

Process consists of:
* text - program code
* data - global and static variables
* heap - dynamically allocated memory
* stack - local variables and function parameters

**Context Switch** - when process is interrupted and another process is executed

**Quantum** - time slice given to process to execute

Process states: (QUZI QUESTION)
* new - process is being created
* ready - process is ready to be executed
* running - process is being executed
* blocked/waiting - process is waiting for something to happen
* terminated - process is finished

**Process Control Block (PCB)** - data structure that contains all information about process like PID, state, priority, memory, registers, etc.

PCB does not contain program variables, code or heap. (QUIZ QUESTION)
