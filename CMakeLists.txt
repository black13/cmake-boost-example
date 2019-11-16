cmake_minimum_required(VERSION 3.10)
SET(Boost_USE_STATIC_LIBS ON)
find_package(Boost REQUIRED regex date_time system filesystem thread graph)
include_directories(${BOOST_INCLUDE_DIRS})
message("boost lib: ${Boost_LIBRARIES}")
message("boost inc:${Boost_INCLUDE_DIR}")

add_executable(use_boost main.cpp)
target_link_libraries(use_boost
        ${Boost_LIBRARIES}
        )

