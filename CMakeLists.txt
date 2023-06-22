cmake_minimum_required(VERSION 3.10)

project(gha_cmake_intel_cpp17_boost)

# C++17
set(CMAKE_CXX_STANDARD 17)

# Cluster things
if(DEFINED ENV{CLUSTER})
  message("Working on cluster")
  # We need to set the compiler on a cluster ourselves,
  # from https://stackoverflow.com/a/45934279
  # (see also there for other (and more recommended) ways)
  set(CMAKE_C_COMPILER "/sw/comp/intel/oneapi/compiler/2023.1.0/linux/bin/icx")
  set(CMAKE_CXX_COMPILER "/sw/comp/intel/oneapi/compiler/2023.1.0/linux/bin/icpx")
else()
  message("Not working on a cluster." )
endif()

# Show compiler info
message("Compiler ID: ${CMAKE_CXX_COMPILER_ID}")
message("Compiler version: ${CMAKE_CXX_COMPILER_VERSION}")

add_executable(gha_cmake_intel_cpp17_boost main.cpp)

# Boost
# See doc at https://cliutils.gitlab.io/modern-cmake/chapters/packages/Boost.html
set(Boost_USE_STATIC_LIBS OFF)
set(Boost_USE_MULTITHREADED ON)
set(Boost_USE_STATIC_RUNTIME OFF)
find_package(Boost 1.50 REQUIRED COMPONENTS graph)
message(STATUS "Boost version: ${Boost_VERSION}")
target_link_libraries(gha_cmake_intel_cpp17_boost PUBLIC Boost::graph)
