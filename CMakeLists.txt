# CMakeList.txt: файл проекта CMake верхнего уровня; проведите глобальную конфигурацию
# и включите сюда подпроекты.
#
cmake_minimum_required (VERSION 3.8)


project ("BattleShipMultiplayer")
#set_property("BattleShipMultiplayer" tgt PROPERTY CXX_STANDARD 20)
# Включите подпроекты.
add_subdirectory ("BattleShipMultiplayer")
