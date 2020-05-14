set (SRC_LIST main.cpp)

set(EXECUTABLE_OUTPUT_PATH ${CMAKETEMPLATE_SOURCE_DIR}/bin)

add_executable(main ${SRC_LIST})

target_link_libraries(main Poco::Net)