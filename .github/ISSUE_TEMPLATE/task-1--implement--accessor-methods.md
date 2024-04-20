---
name: 'Task 1: Implement `SchedulingSystem` member accessor method'
about: Task 1 for Students
title: 'Task 1: Implement `SchedulingSystem` member accessor method'
labels: enhancement, good first issue
assignees: ''

---

**Description**

Implement missing `SchedulingSystem` accessor methods.  You will need to implement
the following 4 missing accessor methods

- `getSystemTime()`
- `getNumProcesses()`
- `isCpuIdle()`
- `getRunningProcessName()`

There are subtask test defines for each of these 4, define the tests
in order and implement these 4 methods.

All of these member methods are accessor methods.  That means they simply
return information about the state of the object, they do not modify
the state of the object.  Therefore all of these accessor methods must
be declared to be `const` member methods.

All methods take no input parameters, as is typical for an accessor method.
Also as is typical, all return an appropriate result type, giving back
the indicated information. The first 2 methods simply return back the
corresponding member variable, but the other 2 need to check the `cpu`
member variable and access the `process` table.

**Suggested Solution**



**Additional Requirements**

- All getter accessor methods must be declared to be `const` member methods.
- All methods must have correctly formatted Doxygen documentation before the
  implementation.  This includes a brief title of the method, a 1 or more
  sentence description, and documentation of input parameters using @param
  and return values using @returns tags.
