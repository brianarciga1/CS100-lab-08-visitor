CMAKE_MINIMUM_REQUIRED(VERSION 2.8)

ADD_SUBDIRECTORY(googletest)

SET(CMAKE_CXX_STANDARD 11)

ADD_EXECUTABLE(calculator
    src/unit_test.cpp
    src/visitor.cpp
    preorder_iterator.cpp
    binary_iterator.cpp
    
)

ADD_EXECUTABLE(test
    main.cpp
)

TARGET_LINK_LIBRARIES(test gtest)
TARGET_COMPILE_DEFINITIONS(test PRIVATE gtest_disable_pthreads=ON)
