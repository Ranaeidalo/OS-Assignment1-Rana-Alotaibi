# Assignment Questions

## Instructions
Answer all 4 questions with detailed explanations. Each answer should be **3-5 sentences minimum** and demonstrate your understanding of the concepts.

---

## Question 1: Thread vs Process

**Question**: Explain the difference between a **thread** and a **process**. Why did we use threads in this assignment instead of creating separate processes?

**Your Answer:A thread is a "lightweight" unit that shares resources inside a process, whereas a process is an autonomous execution unit with its own private memory. Because threads are more effective at emulating a CPU scheduler and provide faster context switching and lower creation overhead, we used them in this assignment. Our program was able to handle several simulated jobs, such as P1 and P2, simultaneously within the same memory area by using threads. This effectively illustrates how contemporary OS schedulers manage multitasking without the high resource requirements of full processes.**

[Write your answer here. Consider: What is a process? What is a thread? How do they differ in terms of memory, resources, creation overhead? Why are threads more suitable for this simulation?]

---

## Question 2: Ready Queue Behavior

**Question**: In Round-Robin scheduling, what happens when a process doesn't finish within its time quantum? Explain using an example from your program output.

**Your Answer:When a process in Round-Robin scheduling is unable to complete its allotted time quantum, it is preempted and returned to the end of the Ready Queue from the Running state. By prohibiting lengthy processes from impeding shorter ones, this method successfully maintains system responsiveness while ensuring fairness. Until the process's remaining time reaches zero, this cycle is repeated.**

[Write your answer here. Describe the specific behavior - where does the process go? When does it run again? Give an example from your actual program output showing a process that was re-queued.]

Example from my output:
▶️ P3 executing quantum [4000ms]
⏸ P3 completed quantum 4000ms │ Remaining time: 5244ms
↻ P3 yields CPU for context switch
➕ P3 added to ready queue │ Burst time: 9244ms │ Priority: 2

**Explanation of example:**
P3 begins with a burst time of 9244 ms, exceeding the 4000 ms quantum, as my output demonstrates. The scheduler pauses P3 after its initial slice, displaying: ↻ P3 yields CPU for context switch. At the conclusion of the queue, the process is re-queued: ➕ P3 added to ready queue. This guarantees that each thread will eventually have access to the CPU.

## Question 3: Thread States

**Question**: A thread can be in different states: **New**, **Runnable**, **Running**, **Waiting**, **Terminated**. Walk through these states for one process (P1) from your simulation.

**Your Answer:**
1. New: Process P1 enters the New state the moment it is created in the simulation, appearing in the system as part of the initial 16 processes.
2. Runnable: It transitions to Runnable as soon as it is added to the queue, as indicated by: ➕ P1 added to ready queue │ Burst time: 2445ms.
3. Running: P1 moves to the Running state when the scheduler picks it first: ▶️ P1 executing quantum [2445ms].
4. Waiting: Interestingly, in my output, P1 does not enter a waiting state after starting because its burst time is smaller than the 4000ms quantum.
5. Terminated: It reaches the Terminated state immediately after finishing its work: ✓ P1 finished execution!, showing a remaining time of 0ms.
By tracing P1, we see how a process with a short burst time can bypass the re-queuing cycle and finish its lifecycle quickly compared to longer processes like P3.

## Question 4: Real-World Applications

**Question**: Give **TWO** real-world examples where Round-Robin scheduling with threads would be useful. Explain why this scheduling algorithm works well for those scenarios.

**Your Answer:**

### Example 1: Web Browsers

**Description**: 
Modern browsers like Chrome use multiple threads to handle various open tabs simultaneously. Each tab operates as a separate task that requires CPU time for rendering content and executing scripts.

**Why Round-Robin works well here**: 
It ensures that a heavy website loading in one tab does not freeze the entire browser UI. By giving each tab a small time slice, the browser remains responsive, allowing users to switch between tabs smoothly without noticeable lag or stuttering.
### Example 2: Smartphone Application Switching

**Description**: 
Modern mobile operating systems use threads to manage multiple background applications and the active user interface (UI) simultaneously. For instance, a phone might be downloading an update, playing music, and waiting for a user to scroll through social media at the same time.

**Why Round-Robin works well here**: 
It ensures the smartphone remains highly responsive to user input by giving the UI thread frequent execution slices. This prevents a heavy background download from "freezing" the screen, as the Round-Robin algorithm quickly cycles through all active tasks. This creates a smooth multitasking experience where every app feels like it is running perfectly in parallel.

## Summary

**Key concepts I understood through these questions:**
1. Threads vs. Processes: I discovered that because threads share memory, they are faster, smaller, and more effective than processes.
2. CPU Fairness: I realized that Round-Robin uses a set time limit (Quantum) to provide each process an equal chance to execute.
3. Queue Movement: I saw how unfinished tasks are moved to the back of the "Ready Queue" to wait for their next turn
   

**Concepts I need to study more:**
1. Thread Synchronization and Race Conditions: I want to look into how operating systems stop several threads from using shared resources at once, which can result in inconsistent data.
2. Dynamic Priority Scheduling: In order to better enhance system efficiency, I'm curious to know how scheduling algorithms can dynamically modify a process's priority based on its behavior and resource utilization.
1. 
2. 
