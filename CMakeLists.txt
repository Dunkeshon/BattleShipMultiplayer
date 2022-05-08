# CMakeList.txt: файл проекта CMake верхнего уровня; проведите глобальную конфигурацию
# и включите сюда подпроекты.
#
cmake_minimum_required (VERSION 3.13)


project ("BattleShipMultiplayer")
if(MSVC)
set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} /std:c++17")
else()
message("Not msvc")
endif(MSVC)
# Включите подпроекты.
add_subdirectory ("BattleShipMultiplayer")

#add_subdirectory ("SFML-build")

#include_directories(${PROJECT_SOURCE_DIR}/)
target_include_directories(${PROJECT_NAME} PRIVATE SFML/SFML-master/include)
target_link_directories(${PROJECT_NAME} PRIVATE SFML/SFML-build/lib/Debug)
#
#find_library(SFML NAMES sfml-graphics-d PATHS ${PROJECT_SOURCE_DIR}/Libs REQUIRED)
#

target_link_libraries(${PROJECT_NAME} PRIVATE sfml-graphics-d 
												sfml-system-d 
												sfml-network-d
												sfml-main-d
												sfml-window-d
												sfml-audio-d)
#find_library(SfmlGraphicsLib sfml-graphics-d REQUIRED) 

