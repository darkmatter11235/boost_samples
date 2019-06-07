cmake_minimum_required(VERSION 3.10.2)

project(boostRtreeTest)

file(GLOB SOURCES "*.cpp")

include_directories("/home/prasanth/EDA/libs/boost_1_70_0")
#set(BOOST_ROOT "/home/prasanth/EDA/libs/boost_1_70_0/boost")
set(BOOST_ROOT "/home/prasanth/EDA/libs/boost_1_70_0")

find_package(Boost REQUIRED COMPONENTS system graph)

add_executable(brt ${SOURCES})

set(PROJECT_LINK_LIBS ${Boost_LIBRARIES})

target_link_libraries(brt ${PROJECT_LINK_LIBS})
