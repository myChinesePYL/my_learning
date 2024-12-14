file(GLOB_RECURSE cpp CONFIGURE_DEPENDS *.cpp **/*.cpp)

add_executable(ml main.cpp ${cpp})

target_include_directories(ml PUBLIC ./)
target_link_libraries(
  ml
  
  glm
  cgc
)
