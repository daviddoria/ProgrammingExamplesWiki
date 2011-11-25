cmake_minimum_required( VERSION 2.6 )

project( StringToValue )

find_package( Boost 1.34 )

if( Boost_FOUND )
  include_directories( ${Boost_INCLUDE_DIRS} )
  add_executable( StringToValue StringToValue.cxx )
else()
  message( "Boost not found" )
endif()
