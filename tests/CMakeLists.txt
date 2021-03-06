add_granite_application(ui-sandbox ui_sandbox.cpp)
target_compile_definitions(ui-sandbox PRIVATE ASSET_DIRECTORY=\"${CMAKE_CURRENT_SOURCE_DIR}/assets\")

add_granite_application(linear-image-test linear_image_test.cpp)
if (NOT ANDROID)
    target_compile_definitions(linear-image-test PRIVATE ASSET_DIRECTORY=\"${CMAKE_CURRENT_SOURCE_DIR}/assets\")
endif()

add_granite_application(mrt-color-mask mrt_color_mask.cpp)
if (NOT ANDROID)
    target_compile_definitions(mrt-color-mask PRIVATE ASSET_DIRECTORY=\"${CMAKE_CURRENT_SOURCE_DIR}/assets\")
endif()

add_granite_application(triangle-test triangle.cpp)
if (NOT ANDROID)
    target_compile_definitions(triangle-test PRIVATE ASSET_DIRECTORY=\"${CMAKE_CURRENT_SOURCE_DIR}/assets\")
endif()

add_granite_application(display-timing-test display_timing.cpp)
if (NOT ANDROID)
    target_compile_definitions(display-timing-test PRIVATE ASSET_DIRECTORY=\"${CMAKE_CURRENT_SOURCE_DIR}/assets\")
endif()

add_granite_application(clustering-visualizer clustering_visualizer.cpp)
target_compile_definitions(clustering-visualizer PRIVATE ASSET_DIRECTORY=\"${CMAKE_CURRENT_SOURCE_DIR}/assets\")

add_granite_application(subgroup-test subgroup.cpp)
target_compile_definitions(subgroup-test PRIVATE ASSET_DIRECTORY=\"${CMAKE_CURRENT_SOURCE_DIR}/assets\")

add_granite_application(fragment-output-components fragment_output_components.cpp)
target_compile_definitions(fragment-output-components PRIVATE ASSET_DIRECTORY=\"${CMAKE_CURRENT_SOURCE_DIR}/assets\")

add_granite_application(basic-compute basic_compute.cpp)
target_compile_definitions(basic-compute PRIVATE ASSET_DIRECTORY=\"${CMAKE_CURRENT_SOURCE_DIR}/assets\")

add_granite_application(pcf-test pcf_test.cpp)
target_compile_definitions(pcf-test PRIVATE ASSET_DIRECTORY=\"${CMAKE_CURRENT_SOURCE_DIR}/assets\")

add_granite_application(cube-array-test cube_array_test.cpp)
target_compile_definitions(cube-array-test PRIVATE ASSET_DIRECTORY=\"${CMAKE_CURRENT_SOURCE_DIR}/assets\")

add_granite_application(render-graph-sandbox render_graph_sandbox.cpp)
target_compile_definitions(render-graph-sandbox PRIVATE ASSET_DIRECTORY=\"${CMAKE_CURRENT_SOURCE_DIR}/assets\")

add_granite_application(bandlimited-pixel-test bandlimited_pixel_test.cpp)
target_compile_definitions(bandlimited-pixel-test PRIVATE ASSET_DIRECTORY=\"${CMAKE_CURRENT_SOURCE_DIR}/assets\")

add_granite_offline_tool(thread-group-test thread_group_test.cpp)
add_granite_offline_tool(intrusive-test intrusive_ptr_test.cpp)
add_granite_offline_tool(ecs-test ecs_test.cpp)
add_granite_offline_tool(simd-test simd_test.cpp)

if (GRANITE_AUDIO)
    add_granite_offline_tool(audio-test audio_test.cpp)
    add_granite_offline_tool(tone-filter-bench tone_filter_bench.cpp)
    target_compile_definitions(audio-test PRIVATE ASSET_DIRECTORY=\"${CMAKE_CURRENT_SOURCE_DIR}/assets\")

    add_granite_application(audio-application audio_application.cpp)
    if (NOT ANDROID)
        target_compile_definitions(audio-application PRIVATE ASSET_DIRECTORY=\"${CMAKE_CURRENT_SOURCE_DIR}/assets\")
    endif()
endif()
