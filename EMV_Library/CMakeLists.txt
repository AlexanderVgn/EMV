file(GLOB EMV_LIB_SOURCES *.cpp)
add_library(EMV STATIC ${EMV_LIB_SOURCES})

target_include_directories(EMV PUBLIC ${CMAKE_CURRENT_SOURCE_DIR})
