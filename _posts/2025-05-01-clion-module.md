---
title: clion module
---

A complete working example

You can try this example in Compiler Explorer and find it on Github.

// a.cppm

````c++
module;

#include <iostream>

export module MyModule;

int hidden() {
    return 42;
}

export void printMessage() {
    std::cout << "The hidden value is " << hidden() << "\n";
}

// main.cpp
import MyModule;

int main() {
    printMessage();
}

# CMakeLists.txt
cmake_minimum_required(VERSION 3.28)

project(modules-example)

set(CMAKE_CXX_STANDARD 20)

add_executable(demo)
target_sources(demo
    PUBLIC
    main.cpp
)
target_sources(demo
  PUBLIC
    FILE_SET all_my_modules TYPE CXX_MODULES FILES
    a.cppm
)
````
