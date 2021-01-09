cmake_minimum_required(VERSION 3.10)


project("fusion-learing" VERSION 1.0)

option(BUILD_KF "build KF" ON)
option(BUILD_EKF "build EKF" ON)


set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED True)
if(BUILD_KF)
	add_subdirectory(KF)
endif()

if(BUILD_EKF)
	add_subdirectory(EKF)
endif()

