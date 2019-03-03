cmake_minimum_required(VERSION 3.13)
project(a53)

set(CMAKE_CXX_STANDARD 14)

add_library(a53 SHARED
        src/a5.c
        src/bits.c
        src/gea.c
        src/kasumi.c
        src/utils.c
        src/ifc.cpp)
target_include_directories(a53 PUBLIC src/include)
set_target_properties(a53 PROPERTIES COMPILE_FLAGS -fPIC)

install(TARGETS a53
        LIBRARY DESTINATION lib)