
python = import('python').find_installation('python3', required : true)

gen_core_tables = [python, files('ggt.py')]
gen_language_headers = [python, files('generate_language_headers.py')]
gen_registry_tables = [python, files('generate_registry_tables.py')]
update_build_version = [python, files('update_build_version.py')]

gen_core_tables_deps = files(
    'Table/__init__.py',
    'Table/Context.py',
    'Table/IndexRange.py',
    'Table/Operand.py',
    'Table/StringList.py',
)
