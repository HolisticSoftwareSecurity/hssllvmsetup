add_library(FunctionPrioritization MODULE src/FunctionPrioritization.cpp)

include_directories(include)

target_compile_features(FunctionPrioritization PRIVATE cxx_range_for cxx_auto_type)

set_target_properties(FunctionPrioritization PROPERTIES
        COMPILE_FLAGS "-g"
        )

if(APPLE)
    set_target_properties(FunctionPrioritization PROPERTIES
            LINK_FLAGS "-undefined dynamic_lookup"
            )
endif(APPLE)
