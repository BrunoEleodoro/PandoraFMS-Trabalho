List of modules used:

# My Custom Module File Exists
module_begin
module_name Check_file_exists
module_type generic_data
module_exec [ -f "/root/nao_apagar.txt" ] && echo 1 || echo 0
module_description Return 1 when file exists return 0 when file not exists
module_group trabalho
module_end
