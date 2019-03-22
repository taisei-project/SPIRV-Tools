
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
)
