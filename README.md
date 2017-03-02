# Autodoc

## Usage

### Comments: Marking code

Code documentation is based on global variables, constants and functions.
Comments on top of globals are exported as formatted code documentation. Example:
```sh
# Check the Git url to clone or update against the banlist.
#  0=do not check at all
#  1=check and accept "unknown" and "non banned" modules.
#  2=check and require "trusted" status for module.
_SECURITY_CHECK_BANNED=1
```

Function comments support more complex descriptions. Format is the function name in the first line, followed by a full description and specific sections: Example, Parameters, Expects and Returns.
Example:
```sh
#==========
# _pp_yaml
#
# Preprocess YAML
#
# Parameters:
#   $1: name of variable to store result in.
#   $2: filepath to read YAML from.
#   $3: filter
#   $4: subdoc
#   $5-x: preprocess variable value assigned to @1, etc.
#
# Expects:
#   _yamlfilelist
#   _SPACEGAL_EOF_TAG
#   _CACHE_LEVEL
#
# Returns:
#   1 if YAML file not found.
#   2 if recursion error occurred.
#   3 if failed to clone modules 
#   4 if assertion failure was triggered.
#
#==========
_pp_yaml()
{
    local _varname=$1
    shift
#.. 
}
```
