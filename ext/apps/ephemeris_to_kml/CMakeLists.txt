# apps/ephemeris_to_kml/CMakeLists.txt

set (HEADERS
    inc/Ephemeris.h
    inc/GeodeticSystemPoint.h
    inc/KMLFile.h)

set (SRC
    src/main.cpp
    src/Ephemeris.cpp
    src/GeodeticSystemPoint.cpp
    src/KMLFile.cpp)

add_executable(ephemeris_to_kml ${SRC} ${HEADERS})
target_link_libraries(ephemeris_to_kml gpstk)
install (TARGETS ephemeris_to_kml DESTINATION "${CMAKE_INSTALL_BINDIR}")
