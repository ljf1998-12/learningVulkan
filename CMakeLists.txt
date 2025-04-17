cmake_minimum_required(VERSION 3.20)

project(learnVulkan LANGUAGES C CXX)
add_executable(${PROJECT_NAME})
target_sources(${PROJECT_NAME} PRIVATE src/main.cpp)
target_compile_features(${PROJECT_NAME} PRIVATE cxx_std_20)

find_package(Vulkan REQUIRED)
target_link_libraries(${PROJECT_NAME} Vulkan::Vulkan)