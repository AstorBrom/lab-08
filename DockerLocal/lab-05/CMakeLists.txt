cmake_minimum_required(VERSION 3.10)
project(bank_test)

set(CMAKE_CXX_STANDARD 17)

set(CMAKE_CXX_STANDARD_REQUIRED ON)

add_library(account STATIC ${CMAKE_CURRENT_SOURCE_DIR}/banking/Account.cpp)
target_include_directories(account
	PUBLIC ${CMAKE_CURRENT_SOURCE_DIR}/banking)

add_library(transaction STATIC ${CMAKE_CURRENT_SOURCE_DIR}/banking/Transaction.cpp)
target_include_directories(transaction
	PUBLIC ${CMAKE_CURRENT_SOURCE_DIR}/banking)
target_link_libraries(transaction account)

#option(BUILD_TESTS "Build test" OFF)

#option(BUILD_COVERAGE "Build code coverage" OFF)
