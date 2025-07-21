file(GLOB UTILITY_SOURCES *.cpp)
add_library(Utility STATIC ${UTILITY_SOURCES})

target_include_directories(Utility PUBLIC ${CMAKE_CURRENT_SOURCE_DIR})
