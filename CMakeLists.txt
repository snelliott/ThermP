project(THERMP Fortran)
cmake_minimum_required(VERSION 2.8)

add_executable(thermp ${PROJECT_SOURCE_DIR}/src/Thermp.f)

install(TARGETS thermp DESTINATION bin)
