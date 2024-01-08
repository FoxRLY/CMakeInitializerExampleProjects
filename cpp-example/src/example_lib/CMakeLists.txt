set(LIB_NAME example_lib)
file(GLOB_RECURSE HEADER_FILES "${CMAKE_SOURCE_DIR}/include/${LIB_NAME}/*.h")
file(GLOB_RECURSE SOURCE_FILES "${CMAKE_SOURCE_DIR}/src/${LIB_NAME}/*.cpp")

add_library(${LIB_NAME} ${SOURCE_FILES} ${HEADER_FILES})
target_include_directories(${LIB_NAME} PUBLIC "${CMAKE_SOURCE_DIR}/include")
