# Unit test
if(CSOAP_ENABLE_UT)
    set(UT_SRCS
        rest_service_manager_test.cc
        )

    set(UT_TARGET_NAME csoap_unittest)

    add_executable(${UT_TARGET_NAME} ${UT_SRCS})
    target_link_libraries(${UT_TARGET_NAME} csoap pugixml gtest)

    add_test(${UT_TARGET_NAME} ${UT_TARGET_NAME})
endif()