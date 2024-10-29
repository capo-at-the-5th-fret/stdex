cmake_minimum_required(VERSION 3.28)

project(stdex
    VERSION 0.1.0
    LANGUAGES CXX
)

add_subdirectory(src)

if (CMAKE_CURRENT_SOURCE_DIR STREQUAL CMAKE_SOURCE_DIR)

    option(STDEX_BUILD_TESTS "Enable or disable the building of tests" ON)
    #option(STDEX_BUILD_EXAMPLES "Enable or disable the building of examples" ON)
    #option(STDEX_BUILD_BENCHMARKS "Enable or disable the building of benchmarks" OFF)
    #option(STDEX_ENABLE_INSTALL "Enable or disable the install rule" ON)

    if (STDEX_BUILD_TESTS)
        enable_testing()
        add_subdirectory(tests)
    endif()

    #if (STDEX_BUILD_EXAMPLES)
     #   add_subdirectory(examples)
    #endif()

    #if (STDEX_BUILD_BENCHMARKS)
    #    add_subdirectory(benchmarks)
    #endif()
endif()

# if (CMAKE_CURRENT_SOURCE_DIR STREQUAL CMAKE_SOURCE_DIR)

#     option(STDEX_BUILD_TESTS "Enable or disable the building of tests" ON)
#     option(STDEX_BUILD_EXAMPLES "Enable or disable the building of examples" ON)
#     option(STDEX_BUILD_BENCHMARKS "Enable or disable the building of benchmarks" ON)
#     #option(STDEX_ENABLE_INSTALL "Enable or disable the install rule" ON)

#     # if (STDEX_BUILD_TESTS)
#     #     enable_testing()
#     #     add_subdirectory(tests)
#     # endif()

#     if (STDEX_BUILD_EXAMPLES)
#         add_subdirectory(examples)
#     endif()

#     # if (STDEX_BUILD_BENCHMARKS)
#     #     add_subdirectory(benchmarks)
#     # endif()

#     # if (STDEX_ENABLE_INSTALL)

#     #     include(GNUInstallDirs)
#     #     include(CMakePackageConfigHelpers)

#     #     # NOTE 1: The XXX_PACKAGE_TARGETS variable is referenced inside of the
#     #     # xxxConfig.cmake.in file, so if the name of this variable changes, it
#     #     # must be updated inside of the xxxConfig.cmake.in file.
#     #     #
#     #     # NOTE 2: If value of this variable changes, the xxxConfig.cmake.in file
#     #     # name must be renamed to match the new value.
#     #     set(STDEX_PACKAGE_NAME ${PROJECT_NAME})
#     #     set(STDEX_PACKAGE_TARGETS ${STDEX_PACKAGE_NAME}Targets)

#     #     set(STDEX_INSTALL_INCLUDE_DIR ${CMAKE_INSTALL_INCLUDEDIR})
#     #     set(STDEX_INSTALL_CMAKE_DIR ${CMAKE_INSTALL_LIBDIR}/cmake/${STDEX_PACKAGE_NAME})

#     #     set(STDEX_CONFIG_DIR ${PROJECT_BINARY_DIR}/cmake)
#     #     set(STDEX_CONFIG_IN cmake/${STDEX_PACKAGE_NAME}Config.cmake.in)
#     #     set(STDEX_CONFIG ${STDEX_CONFIG_DIR}/${STDEX_PACKAGE_NAME}Config.cmake)
#     #     set(STDEX_CONFIG_VERSION ${STDEX_CONFIG_DIR}/${STDEX_PACKAGE_NAME}ConfigVersion.cmake)

#     #     configure_package_config_file(
#     #         ${STDEX_CONFIG_IN}
#     #         ${STDEX_CONFIG}
#     #         INSTALL_DESTINATION ${STDEX_INSTALL_CMAKE_DIR}
#     #     )

#     #     # major.minor.patch1 is compatible with major.minor.patch2..n
#     #     # if no VERSION is specified, the ${PROJECT_VERSION} variable will be
#     #     # used. if the ${PROJECT_VERSION} is not set, CMake will output an
#     #     # error
#     #     write_basic_package_version_file(
#     #         ${STDEX_CONFIG_VERSION}
#     #         COMPATIBILITY SameMinorVersion
#     #     )

#     #     install(
#     #         FILES
#     #             ${STDEX_CONFIG}
#     #             ${STDEX_CONFIG_VERSION}
#     #         DESTINATION ${STDEX_INSTALL_CMAKE_DIR}
#     #     )

#     #     install(TARGETS ${STDEX_PACKAGE_NAME}
#     #         EXPORT ${STDEX_PACKAGE_TARGETS}
#     #         ARCHIVE DESTINATION ${CMAKE_INSTALL_LIBDIR}
#     #         LIBRARY DESTINATION ${CMAKE_INSTALL_LIBDIR}
#     #         RUNTIME DESTINATION ${CMAKE_INSTALL_BINDIR}
#     #     )
        
#     #     install(EXPORT ${STDEX_PACKAGE_TARGETS}
#     #         NAMESPACE ${STDEX_PACKAGE_NAME}::
#     #         DESTINATION ${STDEX_INSTALL_CMAKE_DIR}
#     #     )

#     # endif()

# endif()
