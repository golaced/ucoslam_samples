# ----------------------------------------------------------------------------
#   Basic Configuration
# ----------------------------------------------------------------------------
CMAKE_MINIMUM_REQUIRED(VERSION 2.6)

PROJECT(ucoslam_samples)
set(CMAKE_CXX_STANDARD 11)



#   Find Dependencies
FIND_PACKAGE(OpenCV 	REQUIRED )
FIND_PACKAGE(ucoslam 	REQUIRED )
LINK_LIBRARIES(${OpenCV_LIBS}  ${ucoslam_LIBS} )
#   Add targets
ADD_EXECUTABLE(ucoslam_test_monocular ucoslam_test_monocular.cpp)
ADD_EXECUTABLE(ucoslam_test_stereo ucoslam_test_stereo.cpp)
ADD_EXECUTABLE(ucoslam_test_left_right ucoslam_test_left_right.cpp)
ADD_EXECUTABLE(ucoslam_test_mapiterator ucoslam_test_mapiterator.cpp)

