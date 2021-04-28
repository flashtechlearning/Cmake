cmake_minimum_required(VERSION 3.13.4)

project(LearningPart1)

add_executable(${PROJECT_NAME} main.cpp)

add_subdirectory(external/glfw)
add_subdirectory(calculator)

target_include_directories(${PROJECT_NAME} 
    PUBLIC calculator
    PUBLIC external/glfw/include
)
target_link_directories(${PROJECT_NAME} 
    PRIVATE calculator
    PRIVATE external/glfw/src
)

target_link_libraries(${PROJECT_NAME} 
    calculators_adder
    glfw
)
