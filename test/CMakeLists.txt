# We was inform the Version and project name before, so we didn't need to do that again
file(GLOB SRC_TEST_FILES
        "*.cpp"
)

add_executable(
    GTEST_Test_executable
    ${SRC_TEST_FILES}
)