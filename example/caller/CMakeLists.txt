# set(SRC_LIST calluserservice.cc ../user.pb.cc)
set(SRC_LIST callfriendservice.cc ../friend.pb.cc)

add_executable(consumer ${SRC_LIST})
# target_link_libraries(consumer mprpc protobuf)

# set(CMAKE_PREFIX_PATH "/usr/local/" ${CMAKE_PREFIX_PATH})
# set(CMAKE_INSTALL_RPATH "/usr/local/lib")

find_package(Protobuf REQUIRED)
include_directories(${Protobuf_INCLUDE_DIRS})
target_link_libraries(consumer  mprpc ${Protobuf_LIBRARIES})