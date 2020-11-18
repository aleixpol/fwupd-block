cmake_minimum_required(VERSION 3.18)
project(FwupdBlock)

find_package(Qt5 REQUIRED COMPONENTS Core Concurrent)

find_package(PkgConfig REQUIRED)
pkg_check_modules(Fwupd IMPORTED_TARGET fwupd>=1.0.6)

add_executable(fwupd-block fwupd-block.cpp)
target_link_libraries(fwupd-block Qt::Core Qt::Concurrent PkgConfig::Fwupd)

