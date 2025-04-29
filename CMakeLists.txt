add_library(thirdparty_object OBJECT thirdparty.cpp)
add_library(thirdparty_static STATIC thirdparty.cpp)
target_include_directories(thirdparty_static PUBLIC ${CMAKE_CURRENT_SOURCE_DIR})
target_include_directories(thirdparty_object PUBLIC ${CMAKE_CURRENT_SOURCE_DIR})
