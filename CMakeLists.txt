option(BUILD_THIRDPARTY_STATIC "Build thirdparty as a static library" ON)
option(BUILD_THIRDPARTY_OBJECT "Build thirdparty as an object library" OFF)

set(THIRDPARTY_SOURCES thirdparty.cpp)
set(THIRDPARTY_INCLUDE_DIR ${CMAKE_CURRENT_SOURCE_DIR})

if(BUILD_THIRDPARTY_STATIC)
    add_library(thirdparty STATIC ${THIRDPARTY_SOURCES})
    target_include_directories(thirdparty PUBLIC ${THIRDPARTY_INCLUDE_DIR})
endif()

if(BUILD_THIRDPARTY_OBJECT)
    add_library(thirdparty_object OBJECT ${THIRDPARTY_SOURCES})
    target_include_directories(thirdparty_object PUBLIC ${THIRDPARTY_INCLUDE_DIR})
endif()
