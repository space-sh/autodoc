# Autodoc: code documentation exporter | [![build status](https://gitlab.com/space-sh/autodoc/badges/master/build.svg)](https://gitlab.com/space-sh/autodoc/commits/master)

Generates Markdown documentation based on code comments surrounding global variables and procedures in shell scripts.



## /export/
	Generate module code documentation and export as a Markdown file

	Takes a module shell script code as input, parse all its comments and generate a
	Markdown formatted documentation file as intermediate file. This output gets appended
	to a customized module header and it is exported to the current directory as result.
	If GENERATE_TOC environment variable is set to 1, documentation will
	automatically generate and include table of contents section.
	If GENERATE_VARIABLES environment variable is set to 0, documentation will
	not export the Variables section.
	Parameters:
	    1: module shell script (Spacefile)
	Example:
	    GENERATE_VARIABLES=0 GENERATE_TOC=0 space -m autodoc /module/ -- Spacefile.sh
	


# Functions 

## AUTODOC\_DEP\_INSTALL()  
  
  
  
Check for module dependencies  
  
### Returns:  
- non-zero on failure  
  
  
  
## AUTODOC\_GENERATE\_DOC()  
  
GENERATE\_DOC  
  
Output markdown file  
  
### Parameters:  
- $1: documentation name  
  
### Returns:  
- non-zero on failure  
  
  
  
## AUTODOC\_EXPORT\_MODULE()  
  
EXPORT\_MODULE  
  
Main module documentation exporter  
  
### Parameters:  
- $1: documentation name  
  
### Returns:  
- non-zero on failure  
  
  
  
