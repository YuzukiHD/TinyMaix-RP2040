cmake_minimum_required(VERSION 3.1)

project(cifar10)

add_executable(${PROJECT_NAME} main.c)
target_link_libraries(${PROJECT_NAME} m tinymaix)

# Link with the pico stdlib
target_link_libraries(${PROJECT_NAME} pico_stdlib)

# Create map/bin/hex/uf2 files
pico_add_extra_outputs(${PROJECT_NAME})

# Enable USB serial
pico_enable_stdio_usb(${PROJECT_NAME} 1)
pico_enable_stdio_uart(${PROJECT_NAME} 0)