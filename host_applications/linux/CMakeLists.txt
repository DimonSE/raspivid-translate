# linux apps

if(NOT ARM64)
   add_subdirectory(libs/bcm_host)
endif()

if(NOT ARM64)
   add_subdirectory(apps/raspicam)
   add_subdirectory(libs/sm)
endif()
add_subdirectory(libs/debug_sym)
add_subdirectory(apps/spi_test)

if(ALL_APPS)
 add_subdirectory(libs/elftoolchain)
endif()

