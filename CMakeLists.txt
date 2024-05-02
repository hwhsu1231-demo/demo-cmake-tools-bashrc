cmake_minimum_required(VERSION 3.23)
project(demo-cmake-tools-bashrc)

message(STATUS "----------------------------------------")

find_program(JEKYLL_EXECUTABLE  NAMES jekyll)
find_program(NODE_EXECUTABLE    NAMES node)
find_program(PO4A_EXECUTABLE    NAMES po4a)
find_program(MDBOOK_EXECUTABLE  NAMES mdbook)
find_program(CROWDIN_EXECUTABLE NAMES crowdin)
message(STATUS "JEKYLL_EXECUTABLE   = ${JEKYLL_EXECUTABLE}")
message(STATUS "NODE_EXECUTABLE     = ${NODE_EXECUTABLE}")
message(STATUS "PO4A_EXECUTABLE     = ${PO4A_EXECUTABLE}")
message(STATUS "MDBOOK_EXECUTABLE   = ${MDBOOK_EXECUTABLE}")
message(STATUS "CROWDIN_EXECUTABLE  = ${CROWDIN_EXECUTABLE}")

message(STATUS "ENV{SHELL}          = $ENV{SHELL}")
message(STATUS "ENV{BASH_VERSION}   = $ENV{BASH_VERSION}")
message(STATUS "ENV{PATH}           = $ENV{PATH}")
execute_process(COMMAND env OUTPUT_VARIABLE ENV_CMD_OUT)
message(STATUS "ENV_CMD_OUT         =\n"
               "${ENV_CMD_OUT}")

if(EXISTS "$ENV{HOME}/.bashrc")
    message(STATUS "File \"$ENV{HOME}/.bashrc\" exists.")
endif()
message(STATUS "----------------------------------------")
