cmake_minimum_required(VERSION 3.10)
project(EMV CXX)

# Add subdirectories for libraries
add_subdirectory(Utility)
add_subdirectory(EMV_Library)
add_subdirectory(Runtime)

add_executable(emv emv.cpp)

target_include_directories(emv PRIVATE 
    ${PROJECT_SOURCE_DIR}/Utility
    ${PROJECT_SOURCE_DIR}/EMV_Library
    ${PROJECT_SOURCE_DIR}/Runtime
    ${PROJECT_SOURCE_DIR}/Runtime/RSA
)

target_link_libraries(emv PRIVATE
    Utility
    EMV
    Runtime
    pcsclite
    cryptocme_fips140
    resolv
    pthread
)
