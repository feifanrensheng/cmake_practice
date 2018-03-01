# 声明要求的 cmake 最低版本
CMAKE_MINIMUM_REQUIRED( VERSION 2.8 )

# 声明一个 cmake 工程
PROJECT(SAYHELLO)

# 设置编译模式
SET( CMAKE_BUILD_TYPE "Release")

# 添加头文件路径
INCLUDE_DIRECTORIES(${PROJECT_SOURCE_DIR}/include)

# 添加一个共享库
ADD_LIBRARY( hello SHARED ${PROJECT_SOURCE_DIR}/src/hello.c)

# 添加一个可执行文件
ADD_EXECUTABLE( sayhello useHello.c)

# 将库文件链接到可执行程序上
TARGET_LINK_LIBRARIES( sayhello hello)

# 安装库文件
INSTALL(TARGETS hello LIBRARY DESTINATION lib)

# 安装头文件
INSTALL(FILES ${PROJECT_SOURCE_DIR}/include/hello.h DESTINATION include)
