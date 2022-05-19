# ar-class-2022-hw3
A `dep` file is partitioned into blocks. 
The blocks are separated by a blank line.
Each block except for the last one must begin with a line of the form:
```
package: <package-name>
```
followed by a line of the form 
```
Depends: <package-name1>|<package-name2>,...
```
and/or a line of the form:
```
Conflicts: <package-name1>,...
```

The last line of the file has the form:
```
Install: <package-name1>,...
```

The meaning of such a file was explained in class.

This repository contains some example `dep` files. 
The program you are implementing should either output `There is no installation plan` or
`There is an installation plan`.
In the latter case, starting from the second line of the output, the installation plan should be printed, each package in its own line.

Below is the expected results for these files:
```
$ python3 install_bool.py benchmarks/ex1.dep
There is an installation plan:
apache
c

$ python3 install_bool.py benchmarks/ex2.dep
There is no installation plan

$ python3 install_bool.py benchmarks/ex3.dep
There is an installation plan:
apt
java
apache

$ python3 install_bool.py benchmarks/ex4.dep
There is no installation plan
```

Your implementation will be tested on other files as well.

Important note: it is OK if your implementation suggests a different installation plan.

