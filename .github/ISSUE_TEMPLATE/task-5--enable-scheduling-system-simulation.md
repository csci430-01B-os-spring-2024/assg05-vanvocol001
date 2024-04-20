---
name: 'Task 5: Enable full `SchedulingSystem` simulation'
about: Task 5 for Students
title: 'Task 5: Enable full `SchedulingSystem` simulation'
labels: enhancement
assignees: ''
---

**Description**

Uncomment disabled code in the `SchedulingSystem` implementation file to
enable full simulations.  Check the following member functions to find
disable code and make sure it is enabled:

- `runSimulation()`  need to uncomment the main loop, which is using your
  `allProcessesDone()` `dispatchCpuIfIdle()` and other methods you implemented
  in previous tasks.

Once you enable the `runSimulation()` main loop, your task 5 tests of full
simulations should pass.  And in addition, if you run the system tests, the
FCFS system tests should now be passing for your code.

**Suggested Solution**


**Additional Requirements**

