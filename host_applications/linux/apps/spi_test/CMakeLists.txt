
# test spi app

SET(COMPILE_DEFINITIONS -Werror)

include_directories(${PROJECT_SOURCE_DIR}/host_applications/linux/apps/spi_test/)
include_directories(${PROJECT_SOURCE_DIR}/host_applications/linux/apps/spi_test/wiringPi/)

add_executable(spi_test spi_test.c 
    wiringPi/wiringPi.c 
    wiringPi/wiringPiSPI.c
    wiringPi/softPwm.c
    wiringPi/softTone.c
    wiringPi/piHiPri.c)

target_link_libraries(spi_test   pthread rt)

install(TARGETS spi_test RUNTIME DESTINATION bin)
