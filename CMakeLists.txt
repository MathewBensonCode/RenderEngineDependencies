cmake_minimum_required (VERSION 3.25...4.4 FATAL_ERROR)

project (RendererEngine-Dependencies
    DESCRIPTION "Dependencies for the Renderer Engine Project"
	LANGUAGES CXX
)

include(FetchContent)

FetchContent_Declare(
  fmt
  GIT_REPOSITORY https://github.com/fmtlib/fmt.git
  GIT_SHALLOW TRUE
  GIT_TAG main
    )

FetchContent_Declare(
  imgui
  GIT_REPOSITORY https://github.com/MathewBensonCode/imgui-docking-cmake.git
  GIT_SHALLOW TRUE
  GIT_TAG docking-cmake
  )

FetchContent_Declare(
  ImGuizmo
  GIT_REPOSITORY https://github.com/MathewBensonCode/ImGuizmo.git
  GIT_SHALLOW TRUE
  GIT_TAG imguizmo-cmake
  )

FetchContent_Declare(
  stb
  GIT_REPOSITORY https://github.com/MathewBensonCode/stb.git
  GIT_SHALLOW TRUE
  GIT_TAG stbwithcmake
  )

FetchContent_Declare(
  glfw3
  GIT_REPOSITORY https://github.com/glfw/glfw.git
  GIT_SHALLOW TRUE
  GIT_TAG 3.3.10
  )

FetchContent_Declare(
  spdlog
  GIT_REPOSITORY https://github.com/gabime/spdlog.git
  GIT_SHALLOW TRUE
  GIT_TAG v1.15.3 
  )

FetchContent_Declare(
  EnTT 
  GIT_REPOSITORY https://github.com/skypjack/entt.git
  GIT_SHALLOW TRUE 
  GIT_TAG v3.16.0
  )

FetchContent_Declare(
  assimp
  GIT_REPOSITORY https://github.com/assimp/assimp.git
  GIT_SHALLOW TRUE
  GIT_TAG v6.0.5
  )

FetchContent_Declare(
  stduuid
  GIT_REPOSITORY https://github.com/mariusbancila/stduuid.git
  GIT_SHALLOW TRUE
   
  )

FetchContent_Declare(
  yaml-cpp
  GIT_REPOSITORY https://github.com/jbeder/yaml-cpp
  GIT_SHALLOW TRUE
  )


FetchContent_Declare(
  spirv_cross_core
  GIT_REPOSITORY https://github.com/KhronosGroup/SPIRV-Cross.git
  GIT_TAG vulkan-sdk-1.3.296.0
  GIT_SHALLOW TRUE
  )

FetchContent_Declare(
  VulkanMemoryAllocator
  GIT_REPOSITORY https://github.com/GPUOpen-LibrariesAndSDKs/VulkanMemoryAllocator
  GIT_SHALLOW TRUE
  GIT_TAG v3.3.0
)

FetchContent_Declare(
    SPIRV-Headers
    GIT_REPOSITORY https://github.com/KhronosGroup/SPIRV-Headers.git
    GIT_SHALLOW TRUE
    GIT_TAG vulkan-sdk-1.3.296.0
)

FetchContent_Declare(
    glslang
    GIT_REPOSITORY https://github.com/KhronosGroup/glslang.git
    GIT_SHALLOW TRUE
    GIT_TAG 15.0.0
    SOURCE_DIR "${FETCHCONTENT_BASE_DIR}/glslang"
    
)

FetchContent_Declare(
    SPIRV-Tools
    GIT_REPOSITORY https://github.com/KhronosGroup/SPIRV-Tools.git
    GIT_SHALLOW TRUE
    GIT_TAG vulkan-sdk-1.3.296.0
)


Fetchcontent_Declare(
    GTest
    GIT_REPOSITORY https://github.com/google/googletest.git
    GIT_SHALLOW TRUE
    GIT_TAG main 
)

Fetchcontent_Declare(
  nlohmann_json
    GIT_REPOSITORY https://github.com/nlohmann/json.git
    GIT_SHALLOW TRUE
)

Fetchcontent_Declare(
    tlsf
    GIT_REPOSITORY https://github.com/MathewBensonCode/tlsf
    GIT_TAG tlsf-cmake
    GIT_SHALLOW TRUE
)

Fetchcontent_Declare(
    CLI11
    GIT_REPOSITORY https://github.com/CLIUtils/CLI11
    GIT_SHALLOW TRUE
    GIT_TAG main
)


Fetchcontent_Declare(
    rapidhash
    GIT_REPOSITORY https://github.com/MathewBensonCode/rapidhash
    GIT_TAG rapidhashcmake
    GIT_SHALLOW TRUE
)

FetchContent_Declare(VulkanHeaders
    GIT_REPOSITORY https://github.com/KhronosGroup/Vulkan-Headers
    GIT_SHALLOW TRUE
    GIT_TAG vulkan-sdk-1.3.296.0
)
	
FetchContent_Declare(VulkanLoader
    GIT_REPOSITORY https://github.com/KhronosGroup/Vulkan-Loader
    GIT_SHALLOW TRUE
    GIT_TAG vulkan-sdk-1.3.296.0
)

FetchContent_Declare(miniz
    GIT_REPOSITORY https://github.com/richgel999/miniz
    GIT_SHALLOW TRUE
)


set(CACHE BUILD_EXTERNAL TYPE BOOL OFF)

set(CACHE FMT_TEST TYPE BOOL OFF)
set(CACHE FMT_INSTALL TYPE BOOL ON)

set(CACHE SPDLOG_FMT_EXTERNAL TYPE BOOL ON)
set(CACHE SPDLOG_FMT_EXTERNAL_HO TYPE BOOL OFF)
set(CACHE SPDLOG_INSTALL TYPE BOOL ON)

set(CACHE GLFW_BUILD_DOCS TYPE BOOL OFF)
set(CACHE GLFW_BUILD_EXAMPLES TYPE BOOL OFF)

set(CACHE ASSIMP_BUILD_TESTS TYPE BOOL OFF)
set(CACHE ASSIMP_INSTALL TYPE BOOL ON)
set(CACHE ASSIMP_BUILD_SAMPLES TYPE BOOL OFF)
set(CACHE ASSIMP_BUILD_ASSIMP_TOOLS TYPE BOOL OFF)
set(CACHE ASSIMP_BUILD_ALL_IMPORTERS_BY_DEFAULT TYPE BOOL OFF)
set(CACHE ASSIMP_BUILD_OBJ_IMPORTER TYPE BOOL ON)
set(CACHE ASSIMP_BUILD_ALL_EXPORTERS_BY_DEFAULT TYPE BOOL OFF)
set(CACHE ASSIMP_BUILD_OBJ_EXPORTER TYPE BOOL ON)
set(CACHE ASSIMP_WARNINGS_AS_ERRORS TYPE BOOL OFF)

set(CACHE UUID_BUILD_TESTS TYPE BOOL OFF)
set(CACHE UUID_USING_CXX20_SPAN TYPE BOOL ON)
set(CACHE UUID_SYSTEM_GENERATOR TYPE BOOL OFF)
set(CACHE UUID_ENABLE_INSTALL TYPE BOOL ON)

set(CACHE YAML_CPP_BUILD_TOOLS TYPE BOOL OFF)
set(CACHE YAML_CPP_BUILD_TESTS TYPE BOOL OFF)
set(CACHE YAML_CPP_FORMAT_SOURCE TYPE BOOL OFF)
set(CACHE YAML_BUILD_SHARED_LIBS TYPE BOOL OFF)
set(CACHE YAML_CPP_INSTALL TYPE BOOL ON)

set(CACHE SPIRV_SKIP_EXECUTABLES TYPE BOOL ON)
set(CACHE SPIRV_SKIP_TESTS TYPE BOOL ON)
set(CACHE SPIRV_WERROR TYPE BOOL OFF)
set(CACHE SPIRV_CROSS_WERROR TYPE BOOL OFF)
set(CACHE SPIRV_CROSS_ENABLE_TESTS TYPE BOOL OFF)
set(CACHE SPIRV_CROSS_ENABLE_INSTALL TYPE BOOL ON)
set(CACHE SPIRV_HEADERS_ENABLE_INSTALL TYPE BOOL ON)
set(CACHE ALLOW_EXTERNAL_SPIRV_TOOLS TYPE BOOL ON)

set(CACHE GLSLANG_ENABLE_INSTALL TYPE BOOL ON)

set(CACHE ENTT_INSTALL TYPE BOOL ON)

set(CACHE VULKAN_HEADERS_ENABLE_INSTALL TYPE BOOL ON)
set(CACHE VMA_ENABLE_INSTALL TYPE BOOL ON)
set(CACHE ENTT_INCLUDE_HEADERS TYPE BOOL ON)

set(CACHE JSON_Install TYPE BOOL ON)
set(CACHE CLI11_SINGLE_FILE TYPE BOOL ON)
set(CACHE CLI11_FULL_INSTALL TYPE BOOL ON)
set(CACHE INSTALL_PROJECT TYPE BOOL ON) #miniz install

FetchContent_MakeAvailable(
  fmt
  VulkanHeaders
  VulkanLoader
  imgui
  ImGuizmo
  stb
  glfw3
  spdlog
  EnTT
  assimp
  stduuid
  yaml-cpp
  VulkanMemoryAllocator
  SPIRV-Headers
  spirv_cross_core
  nlohmann_json
  tlsf
  CLI11
  rapidhash
  SPIRV-Tools
  glslang
  GTest
  miniz
  )


add_library(External_libs INTERFACE)

target_link_libraries(External_libs
    INTERFACE
         Vulkan::Headers
         Vulkan::Loader
         glfw
         fmt::fmt
         imgui::imgui
         ImGuizmo::ImGuizmo
         stb::stb
         rapidhash::rapidhash
         tlsf::tlsf
         spdlog::spdlog
         EnTT::EnTT
         assimp::assimp
         stduuid
         yaml-cpp::yaml-cpp
         spirv-cross-core
         SPIRV-Tools-opt
         glslang::glslang
         glslang::glslang-default-resource-limits
         glslang::SPIRV
         GPUOpen::VulkanMemoryAllocator 
         nlohmann_json::nlohmann_json
        CLI11::CLI11
)

set_target_properties(External_libs PROPERTIES INSTALL_RPATH ${CMAKE_INSTALL_PREFIX}/lib)

   install(TARGETS External_libs)

