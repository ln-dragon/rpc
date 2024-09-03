# set(SRC_LIST userservice.cc ../user.pb.cc)
set(SRC_LIST friendservice.cc ../friend.pb.cc)

add_executable(provider ${SRC_LIST})
target_link_libraries(provider mprpc protobuf)

set(CMAKE_PREFIX_PATH "/usr/local/" ${CMAKE_PREFIX_PATH})
set(CMAKE_INSTALL_RPATH "/usr/local/lib")

find_package(Protobuf REQUIRED)
include_directories(${Protobuf_INCLUDE_DIRS})
target_link_libraries(provider  ${Protobuf_LIBRARIES})