cmake_minimum_required(VERSION 3.3)

project(boost_core)

add_library(boost_core INTERFACE)

target_include_directories(boost_core BEFORE INTERFACE ${CMAKE_CURRENT_SOURCE_DIR}/include)

target_link_libraries(boost_core
  INTERFACE boost::assert
  INTERFACE boost::config)

install(TARGETS boost_core DESTINATION lib)
install(DIRECTORY ${CMAKE_CURRENT_SOURCE_DIR}/include/boost DESTINATION include)

add_library(boost::core ALIAS boost_core)
