find_package(PkgConfig REQUIRED)
pkg_check_modules(MYSQL REQUIRED mysqlclient)

include_directories(${MYSQL_INCLUDE_DIRS})
link_directories(${MYSQL_LIBRARY_DIRS})

add_executable(CreationBD CreationBD.cpp)

target_link_libraries(CreationBD ${MYSQL_LIBRARIES})
