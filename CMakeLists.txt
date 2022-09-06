cmake_minimum_required(VERSION 3.15)

project(Freeverb3)

add_library(revmodel
        Freeverb3/Components/allpass.cpp
        Freeverb3/Components/comb.cpp
        Freeverb3/Components/revmodel.cpp
        Freeverb3/Components/tuning.h
        )
target_include_directories(revmodel PUBLIC ${CMAKE_CURRENT_SOURCE_DIR}/Freeverb3/Components)

set(JUCE_SOURCE_DIR "/Users/user/Documents/develop/JUCE")
if(NOT JUCE_SOURCE_DIR)
    message(FATAL_ERROR "JUCE_SOURCE_DIR is empty")
endif()
add_subdirectory(${JUCE_SOURCE_DIR} ${CMAKE_BINARY_DIR}/juce)

add_subdirectory(juce_plugin)