cmake_minimum_required (VERSION 3.14)
SET (CMAKE_C_COMPILER_WORKS 1)
SET (CMAKE_CXX_COMPILER_WORKS 1)
# Define the project
project (testcmsisdsp VERSION 0.1)

# Define the path to CMSIS-DSP (ROOT is defined on command line when using cmake)
# include_directories(${ROOT}/CMSIS/DSP/Toolchain/)#
# include(${ROOT}/CMSIS/DSP/Toolchain/Tools.cmake)

# include(${ROOT}/CMSIS/DSP/Toolchain/AC5.cmake)

# include(${ROOT}/CMSIS/DSP/configLib.cmake)
set(DSP ${ROOT}/CMSIS/DSP)

# Add DSP folder to module path
list(APPEND CMAKE_MODULE_PATH ${DSP})

########### 
#
# CMSIS DSP
#

# Load CMSIS-DSP definitions. Libraries will be built in bin_dsp
add_subdirectory(${DSP}/Source bin_dsp)