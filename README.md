# gettext-tools
This project contains various tools for working with .po (gettext) files.

## msgintersect
> A Gettext .PO file intersection tool.

Generates the intersection between two .PO files.

### Usage

```shell
msgintersect complete-translation.po partially-translated-subset.po fully-translated-subset.po
```

## msgchecker
Checks a PO file for various offenses.

## Usage

```bash
msgchecker [--fix source.po] target.po
```

The `target.po` file will be analysed with the available checks.

Providing a `source.po` file with the `--fix` option will cause the tool to 
try to use available translations from `source.po` to fix failing checks in 
`target.po`. The result will be written back to `target.po`.  

### Current checks
- Checks whether non-empty plurals are identical to the singular form.