# Full S390x JIT support for LuaJIT

## Description
The [LuaJIT](https://github.com/LuaJIT/LuaJIT) project has been unmaintained for some time and there is a [fork](https://github.com/siddhesh/LuaJIT) that has been incorporating fixes and features, including s390x support.  S390x interpreter support for LuaJIT is functional and incorporated into Fedora.  However, only a subset of the builtin testsuite runs due to JIT support not being implemented for S390x.

This project will involve the following tasks:

  * Implement a JIT compiler for S390x
  * Ensure that all tests in the testsuite run and pass for S390x.  Use the x86_64 results for comparison.

## Additional Information
  * [Latest CI Results](https://ci.linaro.org/job/luajit-siddhesh/)

## Desirable Skills
  * Familiar with compilers and/or JIT
  * Comfortable in C and s390x assembly programming

## Expected Outcome
  * LuaJIT has a functional JIT compiler on S390x
  * Same number of tests run and pass as x86_64

## Difficultly
Medium

## Mentors
  * Siddhesh Poyarekar <siddhesh@gotplt.org>

## Additional Contacts
  * luajit@freelists.org
