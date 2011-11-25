cmake_minimum_required( VERSION 2.6 )

project( Lexical_Cast )

find_package( Boost 1.34 )

if( NOT DEFINED ${CMAKE_RUNTIME_OUTPUT_DIRECTORY} )
  set( CMAKE_RUNTIME_OUTPUT_DIRECTORY ${Lexical_Cast_BINARY_DIR}/bin )
endif()

if( Boost_FOUND )
  include_directories( BEFORE ${Boost_INCLUDE_DIRS} )

  add_subdirectory( ValueToString )
  add_subdirectory( StringToValue )

else()
  message( "Boost not found" )
endif()
