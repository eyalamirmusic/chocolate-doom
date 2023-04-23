file(GLOB SHARED_SOURCES Shared/*.c)

add_library(Shared STATIC ${SHARED_SOURCES})
target_link_libraries(Shared PUBLIC
        textscreen
        FluidSynth::libfluidsynth
        opl
        pcsound
        )
target_include_directories(Shared PUBLIC Shared)

file(GLOB DOOM_SOURCES doom/*.c)
add_executable(Doom ${DOOM_SOURCES})
target_link_libraries(Doom PRIVATE
        Shared
        SDL2::SDL2main
        SDL2_mixer::SDL2_mixer
        SDL2_net::SDL2_net
        PNG::PNG)
#target_include_directories()