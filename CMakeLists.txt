cmake_minimum_required(VERSION 2.8)
project( shorelineChangeEstimator )

FILE(GLOB SOURCE_FILES *.cpp)
set(LIBRARIES ${OSSIM_LIBRARIES} ${THIRD_PARTY_LIBRARIES} )
set(INCLUDES ${OSSIM_INCLUDE_DIR} ${THIRD_PARTY_INCLUDE_DIR} ${BOOST_GEOMETRY_LIBRARY})
add_executable( shorelineChangeEstimator ${SOURCE_FILES} )
include_directories( shorelineChangeEstimator ${INCLUDES})
target_link_libraries( shorelineChangeEstimator ${LIBRARIES} )

message("====Project: shorelineChangeEstimator====")
message("====USING THE FOLLOWING LOCATIONS====") 
message("SOURCE FILES:			${SOURCE_FILES}")
message("THIRD_PARTY_INCLUDE_DIR:	${THIRD_PARTY_INCLUDE_DIR}")
message("THIRD_PARTY_LIBRARIES:		${THIRD_PARTY_LIBRARIES}")
message("OSSIM_INCLUDE_DIR:		${OSSIM_INCLUDE_DIR}")
message("OSSIM_LIBRARIES:		${OSSIM_LIBRARIES}")
message("BOOST_C++_LIBRARIES:		${BOOST_GEOMETRY_LIBRARY}")