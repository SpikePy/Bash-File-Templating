# Usage
1. Make the file *tempalte-file* executable by running `chmod +x template-file`
2. Move it to a directory in your `$PATH` or call it directly
5. Run the script with your variables file as argument 1 and your template files as cosecutive arguments
  - The template filename should include the expected file extension appended with '.template'
  - You can call *tempalte-file* with multiple files as arguments, this means they will share the same values
  - you can use wildcards in the arguments as your shell resolves them before the script is executed
  - if you want to use multiple variable files you could `source` another variable file from within the argument-1-variables file
6. The templated result will be stored in your `PWD`

# Variable File

Define you variables in this file just like you define bash variables. You can also use commands as values for variables

# Template File

Write your template as normal text file. Use bash variables e.g. `${USER}` for templating. You can even use commands e.g. `$(date)`


## Example
```bash
cd examples
template-file variables.sh example_static_pod.yaml.template 
```
