本代码是高博slam学习课程第一次作业的第4小题的代码,作为第一次尝试使用github保管代码.以下是作业要求. cmake 是一种常用、方便的,用于组织 Linux 下 C++ 程序的工具。有许多库,例如 OpenCV、g2o、Ceres 等,都用 cmake 组织它们的工程。所以,不管是使用别人的库,还是编写自己的库,都需要掌握一些 cmake 的基本知识。也许你之前没有听过这个工具,但不要紧,我们准备了阅读材料“books/CmakePractice.pdf”( cmake 实践,由一位北大同学撰写)。请阅读此文的第 1 至 6 章,并完成以下工作: 书写一个由 cmake 组织的 C++ 工程,要求如下:

    include/hello.h 和 src/hello.c 构成了 libhello.so 库。hello.c 中提供一个函数 sayHello(),调用此函 数时往屏幕输出一行“Hello SLAM”。我们已经为你准备了 hello.h 和 hello.c 这两个文件,见“code/” 目录下。
    文件 useHello.c 中含有一个 main 函数,它可以编译成一个可执行文件,名为“sayhello”。
    默认用 Release 模式编译这个工程。
    如果用户使用 sudo make install,那么将 hello.h 放至/usr/local/include/下,将 libhello.so 放 至/usr/local/lib/下。 请按照上述要求组织源代码文件,并书写 CMakeLists.txt。
