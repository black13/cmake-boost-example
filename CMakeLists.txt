cmake_minimum_required(VERSION 3.0)
project(boost_log_tutorial)

SET(Boost_USE_STATIC_LIBS ON)           # link statically
#ADD_DEFINITIONS(-DBOOST_LOG_DYN_LINK)  # or, link dynamically

find_package(Boost COMPONENTS log REQUIRED)

add_executable(boost_log_tutorial main.cpp)
target_link_libraries(boost_log_tutorial Boost::log_setup Boost::log)

#sudo apt-get install libboost-dev
#sudo apt-get install emacs
#sudo apt install libboost-regex-dev
#sudo apt-get install libboost-date-time-dev
#sudo apt-get install libboost-system-dev
#sudo apt-get install libboost-filesystem-dev
#sudo apt-get install libboost-thread-dev
#sudo apt-get install libboost-graph-dev
#sudo apt-get install libboost-log-dev
