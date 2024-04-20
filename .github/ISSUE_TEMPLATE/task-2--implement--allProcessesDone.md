---
name: 'Task 2: Implement `allProcessesDone()` member function'
about: Task 2 for Students
title: 'Task 2: Implement `allProcessesDone()` member function'
labels: enhancement
assignees: ''

---

**Description**

Implement the `allProcessesDone()` member method.  This method returns a
`bool` result.  It should return `true` if all processes in the simulation
are done, and false if 1 or more processes are not yet done.  You will need
to use the `process` table and `numProcesses` member variables.  Also the
`process` table consists of an array of `Process` objects, so you need to access
the `done` member variable of a `Process` to determine if each process is done or not.

This member function does not take any parameters as input, and it
returns a `bool` result.  This function does not modifiy the state
of the scheduling simulation, so it should be a `const` member
function.


**Suggested Solution**

```
for each process in the process table
    if the process is not done
	    return false
		
otherwise after the loop all processes checked were done so return true

```


**Additional Requirements**

- The `allProcessesDone()` member method must be declared to be `const`
  member methods as it does not change the simulation state, only
  returns information about current state of memory.
- All methods must have correctly formatted Doxygen documentation before the
  implementation.  This includes a brief title of the method, a 1 or more
  sentence description, and documentation of input parameters using @param
  and return values using @returns tags.


