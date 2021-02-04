cmake_minimum_required(VERSION 3.13.4)

project(LearningPart1)

add_executable(${PROJECT_NAME} main.cpp)

add_subdirectory(adder)

target_include_directories(${PROJECT_NAME} PUBLIC adder)
target_link_directories(${PROJECT_NAME} PRIVATE adder)

target_link_libraries(${PROJECT_NAME} calculators_adder)
