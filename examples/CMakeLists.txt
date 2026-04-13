# Only build examples if enabled
if(NS3_EXAMPLES)

    # ---- leo-orbit ----
    add_executable(leo-orbit
        leo-circular-orbit-tracing-example.cc
    )

    target_link_libraries(leo-orbit
        ${libcore}
        ${libns-3-leo}
        ${libmobility}
    )

    # ---- leo-delay ----
    add_executable(leo-delay
        leo-delay-tracing-example.cc
    )

    set_target_properties(leo-delay PROPERTIES OUTPUT_NAME "leo-delay")

    target_link_libraries(leo-delay
        ${libcore}
        ${libns-3-leo}
        ${libmobility}
        ${libaodv}
        ${libepidemic-routing}
    )

    # ---- leo-bulk-send ----
    add_executable(leo-bulk-send
        leo-bulk-send-example.cc
    )

    target_link_libraries(leo-bulk-send
        ${libcore}
        ${libns-3-leo}
        ${libmobility}
        ${libaodv}
        ${libepidemic-routing}
    )

endif()