# CMakeList.txt: проект CMake для factory; включите исходный код и определения,
# укажите здесь логику для конкретного проекта.
#
cmake_minimum_required (VERSION 3.8)

# Добавьте источник в исполняемый файл этого проекта.
add_executable (factory   "main.cpp" "Vector.h" "Vector.cpp" "VectorVert.h" "VectorVert.cpp" "VectorHor.h" "VectorHor.cpp" "factory.h" "factoryHor.h" "factoryVert.h" "test.h" "test.cpp")
find_package(OpenMP)
if (OPENMP_FOUND)
    set (CMAKE_C_FLAGS "${CMAKE_C_FLAGS} ${OpenMP_C_FLAGS}")
    set (CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} ${OpenMP_CXX_FLAGS}")
    set (CMAKE_EXE_LINKER_FLAGS "${CMAKE_EXE_LINKER_FLAGS} ${OpenMP_EXE_LINKER_FLAGS}")
endif()
#"test.h" "test.cpp"
# TODO: Добавьте тесты и целевые объекты, если это необходимо.
