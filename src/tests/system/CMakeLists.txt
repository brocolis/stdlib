add_executable(test_sleep test_sleep.f90)
target_link_libraries(test_sleep ${PROJECT_NAME})

add_test(NAME Sleep COMMAND $<TARGET_FILE:test_sleep> 350)
set_tests_properties(Sleep PROPERTIES TIMEOUT 1)
