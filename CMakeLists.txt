cmake_minimum_required(VERSION 3.7)
project("PermutedCongruentialGenerator")

add_library("PCG" INTERFACE)
target_compile_features("PCG" INTERFACE cxx_std_11)
target_include_directories("PCG" INTERFACE "include")
