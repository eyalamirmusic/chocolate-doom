cmake_minimum_required(VERSION 3.16)

project(Doom)


find_package(FluidSynth REQUIRED)
find_package(SDL2 REQUIRED)
find_package(SDL2_MIXER REQUIRED)
find_package(SDL2_net REQUIRED)
find_package(PNG REQUIRED)

add_subdirectory(pcsound)
add_subdirectory(opl)
add_subdirectory(textscreen)
add_subdirectory(src)