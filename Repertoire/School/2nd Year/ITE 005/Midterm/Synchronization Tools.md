**Process Synchronization**
Involves using tools that control access to shared data to avoid race conditions.

**Cooperating Process**
Can affect or be affected by other processes executing n the system.
- Share logical address space
- Be allowed to share data only through memory or message passing

**Race Condition**
Situation where several processes access and manipulate the same data concurrently and the outcome of the execution depends on the particular order in which the access takes place.

## Critical-Section Problem
- Consider a system of $n$ processes $[p0, p1, ... pn-1]$
- Each process has a *critical section* segment of code
- may be changing common variables, updating tables, writing files, etc.
- When one process is in a critical section, no other may be in its critical section

**Critical-Section Problem**
- Each process must ask permission to enter critical section in the *entry section*
- may follow critical section with *exit section*
- followed by *remaineder section*

**Requirements for a Solution to a Critical-Section Problem**
- **Mutual Exclusion**
	- Ensures that only one process at a time is active in its critical section
- **Progress**
	- Ensures that programs will cooperatively determine what process will next enter its critical-section
- **Bounded Waiting**
	- Limits how much time a program will wait before it can enter its critical section

### Interrupt-based Solution
**Entry Section:** disable interrupts
**Exit Section:** enable interrupts

## Software Solution 1
- Two process solution
- Assume that the **load** and **store** machine-language instructions are atomic; cannot be interrupted

- 