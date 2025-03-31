idf_component_register(
                    SRCS "nanopb_test.cpp"
                    INCLUDE_DIRS "."
                    PRIV_REQUIRES nanopb
)

find_package(Nanopb REQUIRED)

nanopb_generate_cpp(TARGET proto simple.proto)

target_link_libraries(${COMPONENT_LIB} PRIVATE proto)
