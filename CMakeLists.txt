cmake_minimum_required(VERSION 3.20)


project(Cokoban VERSION 0.0.1 LANGUAGES C)


set(CMAKE_C_STANDARD 23)
set(CMAKE_C_STANDARD_REQUIRED ON)
set(CMAKE_C_EXTENSIONS OFF)


add_executable(Cokoban 
	src/main.c
)

target_include_directories(Cokoban PRIVATE
	include
)


if(MSVC)
	add_compile_options(Cokoban PRIVATE /W4 /WX)
else()
	add_compile_options(Cokoban PRIVATE -Wall -Wextra -Wpedantic -Werror -Wshadow)
endif()
