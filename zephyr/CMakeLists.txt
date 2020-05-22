if(CONFIG_CNL)

zephyr_compile_definitions_ifdef(CONFIG_CNL_USE_UNREACHABLE_UB CNL_USE_UNREACHABLE_UB)
zephyr_compile_definitions_ifdef(CONFIG_CNL_USE_IOSTREAM CNL_USE_IOSTREAM)

zephyr_interface_library_named(Cnl)
zephyr_include_directories(../include)

target_include_directories(Cnl INTERFACE ../include)
target_link_libraries(Cnl INTERFACE zephyr_interface)

endif()