cmake_minimum_required (VERSION 2.6)
project (settings_app)

include_directories(
    include
    ../ui/include
    ../hwcontext/include
)

if(CMAKE_COMPILER_IS_GNUCC)
    set(CMAKE_C_FLAGS "${CMAKE_C_FLAGS} -Wall -pedantic -Wextra -ggdb")
endif()

set(SETTINGS_APP_SOURCES
    settings_main.c
)

add_library(settings_app ${SETTINGS_APP_SOURCES})
set_property(TARGET settings_app PROPERTY C_STANDARD 99)
