cmake_minimum_required(VERSION 3.6)
project(CheckClionConsistency VERSION 1.0.0 LANGUAGES CXX)

include(ExternalProject)
externalproject_add(
        Hunter
        URL "https://github.com/ruslo/hunter/archive/v0.19.234.tar.gz"
        URL_HASH SHA1=3deec1041bd01c91e78269522b901fbab3a765e5
        PATCH_COMMAND ""
        CONFIGURE_COMMAND ""
        BUILD_COMMAND ""
        INSTALL_COMMAND ""
)

add_executable(foo main.cpp)
add_dependencies(foo Hunter)
