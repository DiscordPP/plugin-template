cmake_minimum_required(VERSION 3.6)
project(discordpp-plugin-template)

set(CMAKE_CXX_STANDARD 14)

###################

list(PREPEND ALL_DISCORDPP_PLUGINS discordpp::PluginTemplate
list(APPEND ALL_DISCORDPP_LIBRARIES discordpp-plugin-template)
set(ALL_DISCORDPP_LIBRARIES ${ALL_DISCORDPP_LIBRARIES} PARENT_SCOPE)
set(ALL_DISCORDPP_PLUGINS ${ALL_DISCORDPP_PLUGINS} PARENT_SCOPE)

add_library(${PROJECT_NAME} INTERFACE)

target_include_directories(${PROJECT_NAME} INTERFACE ${CMAKE_CURRENT_SOURCE_DIR})
target_link_libraries(${PROJECT_NAME} INTERFACE )
