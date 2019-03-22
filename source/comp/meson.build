
comp_src = files(
    'bit_stream.cpp',
    'markv.cpp',
    'markv_codec.cpp',
    'markv_decoder.cpp',
    'markv_encoder.cpp',
    'move_to_front.cpp',
)

libspirv_tools_comp = library('SPIRV-Tools-comp',
    comp_src,
    dependencies : [spirv_tools_dep, spvhdr_dep],
    include_directories : private_incdir,
    build_by_default : not meson.is_subproject(),
)

spirv_tools_comp_dep = declare_dependency(
    link_with : libspirv_tools_comp,
    include_directories : public_incdir,
)
