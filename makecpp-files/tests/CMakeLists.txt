project(tests)

link_directories(../lib/test)

add_executable(test_main 
    test_example.cpp
)

target_link_libraries(test_main
    src
    gmock_main
    pthread
)

ADD_TEST(NAME TestMain COMMAND test_main)
