file(GLOB RUNTIME_SOURCES *.cpp)
add_library(Runtime STATIC ${RUNTIME_SOURCES})

target_include_directories(Runtime PUBLIC 
    ${CMAKE_CURRENT_SOURCE_DIR}
    ${CMAKE_CURRENT_SOURCE_DIR}/RSA
)
