add_library(blocky)

file(GLOB_RECURSE blocky_SRC CONFIGURE_DEPENDS "*.cpp")
file(GLOB_RECURSE blocky_HDR CONFIGURE_DEPENDS "*.h")

# Add source files
target_sources(blocky
    PRIVATE
        ${blocky_SRC}
    PUBLIC
        ${blocky_HDR}
)

# Add include directory for header file
target_include_directories(blocky
    PUBLIC
        ${CMAKE_CURRENT_LIST_DIR}/include
)