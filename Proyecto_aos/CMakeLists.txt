cmake_minimum_required(VERSION 3.17)
project(Proyecto_aos)

set(CMAKE:CXX_STANDARD 20)
add_compile_options(-Wall -Wextra -Wno-deprecated -Werror -pedantic -pedantic-errors -fopenmp -DCMAKE_BUILD_TYPE=Release)
find_package(OpenMP REQUIRED)
add_executable(Proyecto_aos sim-aos.hpp sim-aos.cpp calculations.cpp calculations.hpp)
target_link_libraries (Proyecto_aos PUBLIC OpenMP::OpenMP_CXX)
