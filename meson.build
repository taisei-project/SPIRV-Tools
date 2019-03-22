project('SPIRV-Tools', 'cpp',
    version : '2020.2',
    meson_version : '>=0.48.0',
    default_options : [
        'cpp_std=gnu++11',
    ]
)

spvhdr_proj = subproject('SPIRV-Headers')
spvhdr_dep = spvhdr_proj.get_variable('spirv_headers_dep')
spvhdr_incpath = spvhdr_proj.get_variable('spirv_include_path')

file_spir_v_xml = spvhdr_proj.get_variable('file_spir_v_xml')
file_unified1_extinst_debuginfo_grammar_json = spvhdr_proj.get_variable('file_unified1_extinst_debuginfo_grammar_json')
file_unified1_extinst_glsl_std_450_grammar_json = spvhdr_proj.get_variable('file_unified1_extinst_glsl_std_450_grammar_json')
file_unified1_extinst_opencl_debuginfo_100_grammar_json = spvhdr_proj.get_variable('file_unified1_extinst_opencl_debuginfo_100_grammar_json')
file_unified1_extinst_opencl_std_100_grammar_json = spvhdr_proj.get_variable('file_unified1_extinst_opencl_std_100_grammar_json')
file_unified1_extinst_spv_amd_gcn_shader_grammar_json = spvhdr_proj.get_variable('file_unified1_extinst_spv_amd_gcn_shader_grammar_json')
file_unified1_extinst_spv_amd_shader_ballot_grammar_json = spvhdr_proj.get_variable('file_unified1_extinst_spv_amd_shader_ballot_grammar_json')
file_unified1_extinst_spv_amd_shader_explicit_vertex_parameter_grammar_json = spvhdr_proj.get_variable('file_unified1_extinst_spv_amd_shader_explicit_vertex_parameter_grammar_json')
file_unified1_extinst_spv_amd_shader_trinary_minmax_grammar_json = spvhdr_proj.get_variable('file_unified1_extinst_spv_amd_shader_trinary_minmax_grammar_json')
file_unified1_spirv_core_grammar_json = spvhdr_proj.get_variable('file_unified1_spirv_core_grammar_json')

cxx = meson.get_compiler('cpp')

add_project_arguments(cxx.get_supported_arguments(
    '-fno-exceptions',
    '-fno-rtti',
), language : 'cpp')

project_root = meson.current_source_dir()

private_incdir = include_directories('.', 'source')
public_incdir = include_directories('include')

subdir('utils')
subdir('source')
