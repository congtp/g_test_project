cmake_minimum_required(VERSION 3.22.1)

# Set up the project name
project(GTest_Project)

# Create the option for create a test file
option(BUILD_TEST "Create the test" OFF)

# Tell the CMake where to find the source find
file(GLOB SRC_FILES
        "src/*.cpp"
)

# create a variable to store the include files
set(INC_FILES_DIR
    "inc/"
)

# Make the decision for create a test files
if (BUILD_TEST)
    add_subdirectory(test)
endif()

include_directories(
    ${INC_FILES_DIR}
)

# Tell Cmake Collect all the sources file and create the executable files
add_executable(
    GTest_Project
    ${SRC_FILES}
)

