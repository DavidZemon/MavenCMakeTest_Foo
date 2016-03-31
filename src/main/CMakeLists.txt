include_directories(${CMAKE_CURRENT_LIST_DIR}/include)

add_library(foo STATIC c++/foo.cpp)

install(DIRECTORY ${CMAKE_CURRENT_LIST_DIR}/include
    DESTINATION .
)

install(TARGETS foo
    DESTINATION lib
    EXPORT foo-targets
)
install(EXPORT foo-targets
    DESTINATION lib
)
