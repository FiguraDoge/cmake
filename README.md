An exmaple for my stack overflow problem: https://stackoverflow.com/questions/79453883/how-to-correctly-link-libraries-forobject-lib-and-static-shared-lib-of-itself
The main purpose of this repo is to provide the simplest project to elaborate my question on if link library from OBJECT lib is passing to SHARED/STATIC lib.

The way to reproduce the compile error is by deleting the line 10 & 11 in source/component/CmakeList.txt
An error "undefined reference to `example_common::foo()'"  should be reported after the those two lines are deleted.
