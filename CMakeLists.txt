if(APPLE)
  cmake_minimum_required(VERSION 2.8.11 FATAL_ERROR)
else()
  cmake_minimum_required(VERSION 2.8.7 FATAL_ERROR)
endif()

project(boost_core)

add_library(boost_core INTERFACE GLOBAL)

target_include_directories(boost_core BEFORE PUBLIC ${CMAKE_CURRENT_SOURCE_DIR}/include)
