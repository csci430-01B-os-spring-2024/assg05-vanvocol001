---
name: 'Task 4: Implement `checkProcessFinished()` SchedulingSystem member method'
about: Task 4 for Students
title: 'Task 4: Implement `checkProcessFinished()` SchedulingSystem member method'
labels: enhancement
assignees: ''
---

**Description**

The `checkProcessFinished()` member function needs to be implemented.
This is again a `void` function that returns no result and takes no
parameters as input.  This function will actually do the work to mark
a process as finished in the process table and record its end time, so
it is not a `const` member function.

If the cpu is currently `IDLE` then there is nothing to do, and you
should return immediately (look at the next `checkProcessPreemption()`
for an example).  But if a process is currently running, check the
current running process to see if its timeUsed is equal to or exceeds
the `serviceTime` for the process.  If you look back at the
`simulateCpuCycle()` method, you will see that `timeUsed` is
incremented for a process each cycle it is running on the `cpu`.  So
in the `checkProcessFinished()` function, you can test if the
`timeUsed` has reached the `serviceTime`.  When the process is
finished, you need to perform 3 tasks.
   
1. Record the `endTime` for the running process, as it is now finished.
2. Most important, set the process to be `done`.  Each `Process` has
   a member variable named `done` that will be initially `false`.  When
   all processes are marked as done, then the simulation is finished.
3. Also very important, the `cpu` should now be `IDLE`.  You should set
   the simulator `cpu` member variable to the `IDLE` value, so that
   a new process will be dispatched the next time it is checked to see
   if the `cpu` is currently idle or not.


**Suggested Solution**

The following is an example of pseudocode that will implement the
checking if the process is finished for the simulation:

```
if cpu is idle
   do nothing and return immediately
   
if the process that is running's time used is less than its service time
   then process is not done, so do nothing and return immediately
   
othewise the process is done so
1. record its endTime as the current systemTime
2. mark the process as done
3. set the cpu to be idle again

```

**Additional Requirements**

- You must correctly record the information about the process finishing in the
  process table for use by the simulation.
- All methods must have correctly formatted Doxygen documentation before the
  implementation.  This includes a brief title of the method, a 1 or more
  sentence description, and documentation of input parameters using @param
  and return values using @returns tags.
