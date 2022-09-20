add_library(tinymaix tm_layers.c tm_layers_fp8.c tm_layers_O1.c tm_model.c tm_stat.c)
target_link_libraries(tinymaix m pico_stdlib)