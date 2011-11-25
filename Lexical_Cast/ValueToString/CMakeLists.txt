cmake_minimum_required( VERSION 2.6 )

project( ValueToString )

find_package( Boost 1.34 )

if( Boost_FOUND )
  include_directories( ${Boost_INCLUDE_DIRS} )
  add_executable( ValueToString ValueToString.cxx )
else()
  message( "Boost not found" )
endif()
