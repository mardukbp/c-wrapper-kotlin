# c-wrapper-kotlin
## Attempt to link form kotlin a C++ library wrapped in C API

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

Trying to build the project using gradle yields a link error:
~~~~
vbaggiol@laptop:/tmp$ cd c-wrapper-kotlin
vbaggiol@laptop:/tmp/c-wrapper-kotlin$ gradle build

> Configure project :
feature GRADLE_METADATA is not enabled: publication is disabled

> Task :compileKonanK-wrapperLinux_x64 FAILED
/tmp/included802814211042874970/libmyLib.a(MyWrapper.cpp.o):MyWrapper.cpp:function newMyClass: error: undefined reference to 'operator new(unsigned long)'
error: /home/vbaggiol/.konan/dependencies/target-gcc-toolchain-3-linux-x86-64/x86_64-unknown-linux-gnu/bin/ld.gold invocation reported errors

FAILURE: Build failed with an exception.

* What went wrong:
Execution failed for task ':compileKonanK-wrapperLinux_x64'.
> Process 'command '/usr/lib/jvm/java-8-openjdk-amd64/bin/java'' finished with non-zero exit value 1

* Try:
Run with --stacktrace option to get the stack trace. Run with --info or --debug option to get more log output. Run with --scan to get full insights.

* Get more help at https://help.gradle.org

BUILD FAILED in 13s
3 actionable tasks: 3 executed
vbaggiol@laptop:/tmp/c-wrapper-kotlin$ 
~~~~ 

