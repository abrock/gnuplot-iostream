cmake_minimum_required(VERSION 2.8)
project(gnuplot-iostream)

SET(CMAKE_CXX_FLAGS "-g -O0 -D_GLIBCXX_DEBUG")

FILE(GLOB_RECURSE LibFiles "gnuplot-iostream.h")
add_custom_target(gnuplot-iostream-headers SOURCES ${LibFiles})

add_executable(example-misc example-misc.cc)
target_link_libraries(example-misc util boost_iostreams boost_system boost_filesystem)

add_executable(example-data-1d example-data-1d.cc)
target_link_libraries(example-data-1d util boost_iostreams boost_system boost_filesystem)

add_executable(example-data-2d example-data-2d.cc)
target_link_libraries(example-data-2d util boost_iostreams boost_system boost_filesystem)

add_executable(example-interactive example-interactive.cc)
target_link_libraries(example-interactive util boost_iostreams boost_system boost_filesystem)


