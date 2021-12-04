cmake_minimum_required(VERSION 2.8.11)

project(xrdp-kde)

install(FILES src/xrdp-NetworkManager.pkla DESTINATION  /etc/polkit-1/localauthority/50-local.d/ )
install(FILES src/xrdp-packagekit.pkla DESTINATION  /etc/polkit-1/localauthority/50-local.d/ )
set(CPACK_PACKAGE_NAME "xrdp-kde")
set(CPACK_PACKAGE_DESCRIPTION_SUMMARY "xrdp package for use under kde environment.")
set(CPACK_PACKAGE_VERSION "1.0.0")
set(SYSTEM_ARCH "all")
set(CPACK_DEBIAN_PACKAGE_DEPENDS "xrdp")
set(CPACK_GENERATOR "DEB")
set(PACKAGE_OS "linux")
set(CPACK_SYSTEM_NAME "${PACKAGE_OS}-amd64")
set(SYSTEM_ARCH "amd64")
set(CPACK_DEBIAN_PACKAGE_MAINTAINER "Johannes Maier <maier_jo@gmx.de>")
set(CPACK_DEBIAN_PACKAGE_CONTROL_EXTRA "${CMAKE_CURRENT_SOURCE_DIR}/postinst;${CMAKE_CURRENT_SOURCE_DIR}/prerm;${CMAKE_CURRENT_SOURCE_DIR}/postrm;")
set(CPACK_PACKAGE_FILE_NAME "${CPACK_PACKAGE_NAME}-${CPACK_PACKAGE_VERSION}-${CPACK_DEBIAN_REVISON}${CPACK_SYSTEM_NAME}")

include(CPack)


