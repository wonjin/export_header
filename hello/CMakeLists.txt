
project(hello)

set(CMAKE_CXX_VISIBILITY_PRESET hidden)
set(CMAKE_VISIBILITY_INLINES_HIDDEN YES)

include(GenerateExportHeader)

add_library(hello src/hello.cpp)
target_include_directories(hello PUBLIC 
    include
    ${CMAKE_CURRENT_BINARY_DIR}
)

generate_export_header(hello EXPORT_MACRO_NAME HELLO_API)