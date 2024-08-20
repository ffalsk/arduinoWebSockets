
get_filename_component(dir ${CMAKE_CURRENT_LIST_FILE} PATH)
FILE(GLOB_RECURSE app_sources
    ${dir}/src/*.c
    ${dir}/src/*.cpp
)

idf_component_register(SRCS ${app_sources}
    REQUIRES "arduinoWebSockets"
    INCLUDE_DIRS "src"
    REQUIRES arduino-esp32)
