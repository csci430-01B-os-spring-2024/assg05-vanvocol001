---
name: 'Task 6: Implement Additional Scheduling Policy'
about: Task 6 for Students
title: 'Task 6: Implement Additional Scheduling Policy'
labels: enhancement
assignees: ''
---

**Description**

Implement an additional scheduling policy from scratch.

**Suggested Solution**

You need to do all of the following (among possibly other things):

- Copy the FCFS header and implementation files to new files and rename them
  for the new scheduling policy you will implement.
- Search/replace in the file to change the class name and any other place to reflect
  the new scheduling policy you are implementing.
- Add your new source file to the build system.  Make sure the files is built and linked
  into your `test` and `sim` executables successfully.
- Implement all of the `SchedulingPolicy` API methods for your choosen new
  scheduling policy.
- Add/uncomment code in `assg05-sim.cpp` file to be able to run simulations using your
  new policy from the command line.
- Test your new policy using the system tests at a minimum.  You may find it useful to add
  additional unit tests in `assg05-tests.cpp` while implementing the member methods
  for your scheduling policy.


**Additional Requirements**

