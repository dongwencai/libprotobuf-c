project(protobuf_test)
cmake_minimum_required(VERSION 2.8)
SET(PROTOBUF_C_SRC protobuf-c.c protobuf-c.h)
add_library(protobuf-c STATIC ${PROTOBUF_C_SRC})

set(SRC_LIST student.pb-c.c student.pb-c.h test.c)
add_executable(${PROJECT_NAME} ${SRC_LIST})
target_link_libraries(${PROJECT_NAME} protobuf-c)
