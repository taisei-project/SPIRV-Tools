
reduce_src = files(
    'change_operand_reduction_opportunity.cpp',
    'change_operand_to_undef_reduction_opportunity.cpp',
    'operand_to_const_reduction_pass.cpp',
    'operand_to_dominating_id_reduction_pass.cpp',
    'operand_to_undef_reduction_pass.cpp',
    'reducer.cpp',
    'reduction_opportunity.cpp',
    'reduction_pass.cpp',
    'reduction_util.cpp',
    'remove_instruction_reduction_opportunity.cpp',
    'remove_opname_instruction_reduction_pass.cpp',
    'remove_unreferenced_instruction_reduction_pass.cpp',
    'structured_loop_to_selection_reduction_opportunity.cpp',
    'structured_loop_to_selection_reduction_pass.cpp',
)

libspirv_tools_recude = library('SPIRV-Tools-reduce',
    reduce_src,
    dependencies : [spirv_tools_dep, spirv_tools_opt_dep, spvhdr_dep],
    include_directories : private_incdir,
    build_by_default : not meson.is_subproject(),
)

spirv_tools_reduce_dep = declare_dependency(
    link_with : libspirv_tools_recude,
    include_directories : public_incdir,
)
