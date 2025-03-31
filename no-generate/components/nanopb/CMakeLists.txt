idf_component_register()

include(FetchContent)

FetchContent_Declare(
        nanopb
        OVERRIDE_FIND_PACKAGE
        GIT_REPOSITORY https://github.com/nanopb/nanopb.git
        GIT_TAG        cad3c18ef15a663e30e3e43e3a752b66378adec1
        GIT_PROGRESS   TRUE
        GIT_SHALLOW    TRUE
)

FetchContent_MakeAvailable(nanopb)

target_link_libraries(${COMPONENT_LIB} INTERFACE nanopb)
