option(BUILD_THIRDPARTY_STATIC "Build thirdparty as a static library" ON)
option(BUILD_THIRDPARTY_OBJECT "Build thirdparty as an object library" OFF)

if(BUILD_THIRDPARTY_STATIC)
    add_library(thirdparty STATIC thirdparty.cpp)
    target_include_directories(thirdparty PUBLIC ${CMAKE_CURRENT_SOURCE_DIR})
endif()

if(BUILD_THIRDPARTY_OBJECT)
    add_library(thirdparty_object OBJECT thirdparty.cpp)
    target_include_directories(thirdparty_object PUBLIC ${CMAKE_CURRENT_SOURCE_DIR})
endif()
