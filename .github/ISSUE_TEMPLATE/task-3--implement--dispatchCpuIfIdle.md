---
name: 'Task 3: Implement `dispatchCpuIfIdle()` SchedulingSystem member method'
about: Task 3 for Students
title: 'Task 3: Implement `dispatchCpuIfIdle()` SchedulingSystem member method'
labels: enhancement
assignees: ''

---

**Description**

Implement the `dispatchCpuIfIdle()` member function.

This function is a `void` function that has no parameters as input, nor
does it return an explicit result.  All of its work is done by examing
the current state of the cpu, and working with the scheduling policy to
dispatch a process if the cpu is idle.  This function cannot be a
`const` member function, because it can change the state of the simulation
by changing the `cpu` from being idle to currently running a process.

You will have to access the `policy` to ask it to `dispatch()` a process
if the cpu is currently idle.

**Suggested Solution**

A possible pseudocode implemention of this function is as follows:

```
if cpu is idle
	ask the policy to dispatch the next process to run
	the dispatch method returns the Pid of the process, set cpu to be this process id
	update the startTime of this process if it was never started before
```

**Additional Requirements**

- This method must use the scheduling `policy` instance to do the actual work
  of selecting which process to dispatch next.
- This method must update the `startTime` of the process if this was the first
  time that this process was run in the simulation.
- All methods must have correctly formatted Doxygen documentation before the
  implementation.  This includes a brief title of the method, a 1 or more
  sentence description, and documentation of input parameters using @param
  and return values using @returns tags.


