add_library(stdex STATIC)

target_sources(stdex
    PUBLIC
        FILE_SET CXX_MODULES
        FILES
            stdex.cxx

            utility.cxx
    )

target_compile_features(stdex PUBLIC cxx_std_23)
