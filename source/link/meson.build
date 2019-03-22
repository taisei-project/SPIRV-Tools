
link_src = files(
    'linker.cpp',
)

libspirv_tools_link = library('SPIRV-Tools-link',
    link_src,
    dependencies : [spirv_tools_dep, spirv_tools_opt_dep, spvhdr_dep],
    include_directories : private_incdir,
    build_by_default : not meson.is_subproject(),
)

spirv_tools_link_dep = declare_dependency(
    link_with : libspirv_tools_link,
    include_directories : public_incdir,
    version : meson.project_version(),
)

libspirv_tools_link_native = library('SPIRV-Tools-link-native',
    link_src,
    dependencies : [spirv_tools_native_dep, spirv_tools_opt_native_dep, spvhdr_dep],
    include_directories : private_incdir,
    build_by_default : false,
    native : true,
    override_options : native_options,
)

spirv_tools_link_native_dep = declare_dependency(
    link_with : libspirv_tools_link_native,
    include_directories : public_incdir,
    version : meson.project_version(),
)
