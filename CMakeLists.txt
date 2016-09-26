if(APPLE)
  cmake_minimum_required(VERSION 2.8.11 FATAL_ERROR)
else()
  cmake_minimum_required(VERSION 2.8.7 FATAL_ERROR)
endif()

if(NOT BOOST_CONFIG_INCLUDE_DIRS)
  message(FATAL_ERROR "Cannot find boost.config!")
endif(NOT BOOST_CONFIG_INCLUDE_DIRS)

if(NOT BOOST_ASSERT_INCLUDE_DIRS)
  message(FATAL_ERROR "Cannot find boost.assert!")
endif(NOT BOOST_ASSERT_INCLUDE_DIRS)

set(BOOST_CORE_INCLUDE_DIRS "${CMAKE_CURRENT_SOURCE_DIR}/include" CACHE STRING "Location of boost.core headers")

set(BOOST_INCLUDE_DIRS "${BOOST_INCLUDE_DIRS}" "${BOOST_CORE_INCLUDE_DIRS}" CACHE STRING "All Boost headers" FORCE)
