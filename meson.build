project('SPIRV-Tools', 'cpp',
    version : '2019.4.136',
    meson_version : '>=0.46.0',
    default_options : [
        'cpp_std=c++11',
    ]
)

spvhdr_proj = subproject('SPIRV-Headers')
spvhdr_dep = spvhdr_proj.get_variable('spirv_headers_dep')
spvhdr_incpath = spvhdr_proj.get_variable('spirv_include_path')

file_spir_v_xml = spvhdr_proj.get_variable('file_spir_v_xml')
file_unified1_spirv_core_grammar_json = spvhdr_proj.get_variable('file_unified1_spirv_core_grammar_json')
file_unified1_extinst_glsl_std_450_grammar_json = spvhdr_proj.get_variable('file_unified1_extinst_glsl_std_450_grammar_json')
file_unified1_extinst_opencl_std_100_grammar_json = spvhdr_proj.get_variable('file_unified1_extinst_opencl_std_100_grammar_json')

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
