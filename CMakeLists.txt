cmake_minimum_required(VERSION 2.8)

project(phonetendo)

find_package(SDL REQUIRED)
find_package(SDL_image REQUIRED)
find_package(SDL_sound REQUIRED)
find_package(SDL_mixer REQUIRED)
find_package(SDL_ttf REQUIRED)

include_directories(${SDL_INCLUDE_DIR})

add_executable(phonetendo callin.cpp callout.cpp controller.cpp dtmf.cpp encounter.cpp game.cpp map.cpp misc.cpp nametag.cpp npc.cpp office.cpp route.cpp stapler.cpp tasks.cpp tiles.cpp umec_device.cpp)

set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -g")
target_link_libraries(phonetendo ${SDL_LIBRARY} ${SDLMIXER_LIBRARY} ${SDLTTF_LIBRARY} ${SDLIMAGE_LIBRARY} ${SDL_SOUND_LIBRARY})

