file(GLOB_RECURSE cpp CONFIGURE_DEPENDS *.cpp **/*.cpp)
add_compile_options(-std=c++14 -Wall -Werror -pedantic-errors)

add_executable(ml main.cpp ${cpp})

target_include_directories(ml PUBLIC ./)
target_link_libraries(
  ml
  
  glm
)
