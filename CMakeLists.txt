##---------------------------------------------------------------------------
## Author:      nohal aka. Pavel Kalian
## Copyright:
## License:     wxWidgets License
##---------------------------------------------------------------------------

# define minimum cmake version
CMAKE_MINIMUM_REQUIRED(VERSION 2.6.2)

PROJECT(aisradar_pi)

SET(CMAKE_MACOSX_RPATH "ON")

SET(PACKAGE_NAME aisradar_pi)
SET(VERBOSE_NAME AISRadar)
SET(TITLE_NAME AISRadar)
SET(CPACK_PACKAGE_CONTACT "Johan Sman")

SET(VERSION_MAJOR "1")
SET(VERSION_MINOR "1")
SET(VERSION_PATCH "1")
SET(VERSION_DATE "2019-06-12")
SET(OCPN_VERSION "ov42")

#SET(CMAKE_BUILD_TYPE Debug)

INCLUDE("cmake/PluginConfigure.cmake")

SET(SRC_AISRADAR
      src/aisradar_pi.h
      src/aisradar_pi.cpp
      src/aisradar.h
      src/aisradar.cpp
      src/my_icons.h
      src/my_icons.cpp
      src/Canvas.h
      src/Canvas.cpp
      src/Target.h
      src/Target.cpp
    )
ADD_LIBRARY(${PACKAGE_NAME} SHARED ${SRC_AISRADAR})

INCLUDE("cmake/PluginInstall.cmake")
INCLUDE("cmake/PluginLocalization.cmake")
INCLUDE("cmake/PluginPackage.cmake")
