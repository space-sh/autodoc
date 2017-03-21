---
title: /export/
giturl: gitlab.com/space-sh/autodoc
weight: 200
---
# Autodoc module: Export

Generates module code documentation and export as Markdown file.


## Example

Change directory to any Space Module and run the following command to create an auto generated technical README file:
```sh
space -m autodoc /export/ -- Spacefile.sh
```

Output:
```sh
[INFO]  AUTODOC_GENERATE_DOC: Generating markdown documentation without TOC...
[INFO]  AUTODOC_GENERATE_DOC: Documentation exported to "Spacefile.sh_doc.md"
[INFO]  AUTODOC_EXPORT_MODULE: Generating composed output...
[INFO]  AUTODOC_EXPORT_MODULE: Removing intermediate file "Spacefile.sh_doc.md"
[INFO]  AUTODOC_EXPORT_MODULE: Module documentation exported to "Spacefile.sh_README"
```
