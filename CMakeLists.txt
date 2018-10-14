cmake_minimum_required(VERSION 3.12)
project(qdl C)

find_package(LibXml2 REQUIRED)
include_directories(${CMAKE_CURRENT_SOURCE_DIR} ${LIBXML2_INCLUDE_DIR})

set(CMAKE_C_STANDARD 11)
set(CMAKE_CXX_FLAGS "-O2 -Wall -g")

set(SOURCE_FILES
        qdl.c
        firehose.c
        patch.c
        program.c
        sahara.c
        ufs.c
        util.c
        )

add_executable(qdl ${SOURCE_FILES})
target_link_libraries(qdl ${LIBXML2_LIBRARIES})