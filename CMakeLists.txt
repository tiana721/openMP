cmake_minimum_required (VERSION 3.8)


project (openMP)

set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++1z -fopenmp")

add_executable (openMP  main.cpp Vector.h Vector.cpp VectorVert.h VectorVert.cpp VectorHor.h VectorHor.cpp test.h test.cpp factory.h factoryVert.h factoryHor.h)
