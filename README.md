# gha_cmake_intel_cpp17_boost

Branch   |[![GitHub Actions logo](pics/GitHubActions.png)](https://github.com/richelbilderbeek/gha_cmake_intel_cpp17_boost/actions)
---------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
`master` |[![Check build](https://github.com/richelbilderbeek/gha_cmake_intel_cpp17_boost/actions/workflows/check_build.yml/badge.svg?branch=master)](https://github.com/richelbilderbeek/gha_cmake_intel_cpp17_boost/actions/workflows/check_build.yml)
`develop`|[![Check build](https://github.com/richelbilderbeek/gha_cmake_intel_cpp17_boost/actions/workflows/check_build.yml/badge.svg?branch=develop)](https://github.com/richelbilderbeek/gha_cmake_intel_cpp17_boost/actions/workflows/check_build.yml)

The goal of this project is to have a clean GitHub Actions build, with specs:

 * Build system: `CMake`
 * C++ compiler: Intel
 * C++ version: `C++17`
 * Libraries: `STL` and Boost
 * Code coverage: none
 * Profiling: none
 * Source: one single file, `main.cpp`

More complex builds:

 * [none]

Equally complex builds:

 * Build without the GCC (instead of the Intel) compiler: [gha_cmake_gcc_cpp17_boost](https://github.com/richelbilderbeek/gha_cmake_gcc_cpp17_boost)

Less complex builds:

 * Build without Boost: [gha_cmake_intel_cpp17](https://github.com/richelbilderbeek/gha_cmake_intel_cpp17)
 * Build without `CMake`: [gha_intel_cpp17_boost](https://github.com/richelbilderbeek/gha_intel_cpp17_boost)
 
