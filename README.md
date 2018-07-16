# Use a C++ library wrapped in C API from Kotlin Native

This project dependes on the repository c-wrapper. 
Please check it out to /tmp and build it as described there.

Checkout this project to /tmp:
~~~~
vbaggiol@laptop:~$ cd /tmp
vbaggiol@laptop:/tmp$ git clone https://github.com/vbaggiol/c-wrapper-kotlin.git
git clone https://github.com/vbaggiol/c-wrapper-kotlin.git
Cloning into 'c-wrapper-kotlin'...
remote: Counting objects: 20, done.
remote: Compressing objects: 100% (12/12), done.
remote: Total 20 (delta 2), reused 20 (delta 2), pack-reused 0
Unpacking objects: 100% (20/20), done.
Checking connectivity... done.
~~~~

Build the project using gradle yields a link error:
~~~~
vbaggiol@laptop:/tmp$ cd c-wrapper-kotlin
vbaggiol@laptop:/tmp/c-wrapper-kotlin$ gradle build

vbaggiol@lapbe15342:/tmp/c-wrapper-kotlin$ gradle build

> Configure project :
feature GRADLE_METADATA is not enabled: publication is disabled

BUILD SUCCESSFUL in 14s
3 actionable tasks: 3 executed
vbaggiol@laptop:/tmp/c-wrapper-kotlin$ 
~~~~ 

and execute the resulting kexe:

~~~~
vbaggiol@laptop:/tmp/c-wrapper-kotlin$ ./build/konan/bin/linux_x64/k-wrapper.kexe 
./build/konan/bin/linux_x64/k-wrapper.kexe 
Hello, Native World!
MyClass_int_get(myClass) yields: 22
vbaggiol@laptop:/tmp/c-wrapper-kotlin$ 
~~~~
