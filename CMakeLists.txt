add_executable(test_calc
  test/test_main.cpp
  test/test_calc.cpp
  src/calc.cpp)
target_link_libraries(test_calc
  ${CMAKE_CURRENT_SOURCE_DIR}/third_party/googletest-release-1.8.1/build/googlemock/gtest/libgtest.a
  ${CMAKE_CURRENT_SOURCE_DIR}/third_party/googletest-release-1.8.1/build/googlemock/gtest/libgtest_main.a
  pthread)
target_include_directories(test_calc PUBLIC
  include
  ${CMAKE_CURRENT_SOURCE_DIR}/third_party/googletest-release-1.8.1/googletest/include)
