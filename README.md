```
WIP - Hysterical Historical Attempt to Update for A2R3..
(and then be able to at least not choke if a <3.0 format is encountered.)

A2R2 to A2R3 .. 

✘ tdiaz@ICBM-1701 -> ~/W3_Sandbox/python/a2rchery -> primordial ±✚ -> python3 a2rchery.py dump Apple3UniDuoFile2\ -\ Disk\ 2,\ Side\ A-A2R3.a2r
read_IDa
read_IDb
read2_raw
read_size
read_IDa
read_IDb
read2_raw
read_size
**A2RRWCPFormatError**: Missing phase reset at end of RWCP chunk

(Excuse my lame hardcoded trace method - I don't know any better)

 ✘ tdiaz@ICBM-1701 -> ~/W3_Sandbox/python/a2rchery ->  primordial ±✚ -> python3 a2rchery.py dump Apple3UniDuoFile2\ -\ Disk\ 2,\ Side\ A.a2r


$ ./a2rchery.py verify -h
usage: a2rchery verify [-h] file

Verify file structure and metadata of a .a2r disk image (produces no output
unless a problem is found)

positional arguments:
  file        .a2r disk image

optional arguments:
  -h, --help  show this help message and exit



$ ./a2rchery.py dump -h
usage: a2rchery dump [-h] file

Print all available information and metadata in a .a2r disk image

positional arguments:
  file        .a2r disk image

optional arguments:
  -h, --help  show this help message and exit



$ ./a2rchery.py edit -h
usage: a2rchery edit [-h] [-i INFO] [-m META] file

Edit information and metadata in a .a2r disk image

positional arguments:
  file                  .a2r disk image (modified in place)

optional arguments:
  -h, --help            show this help message and exit
  -i INFO, --info INFO  change information field. INFO format is "key:value".
                        Acceptable keys are disk_type, write_protected,
                        synchronized, creator, version. Other keys are
                        ignored. For boolean fields, use "1" or "true" or
                        "yes" for true, "0" or "false" or "no" for false.
  -m META, --meta META  change metadata field. META format is "key:value".
                        Standard keys are title, subtitle, publisher,
                        developer, copyright, version, language, requires_ram,
                        requires_machine, notes, side, side_name, contributor,
                        image_date. Other keys are allowed.

Tips:

 - Use repeated flags to edit multiple fields at once.
 - Use "key:" with no value to delete a metadata field.
 - Keys are case-sensitive.
 - Some values have format restrictions; read the .a2r specification.

$ ./a2rchery.py export -h
usage: a2rchery export [-h] file

Export (as JSON) all information and metadata from a .a2r disk image

positional arguments:
  file        .a2r disk image

optional arguments:
  -h, --help  show this help message and exit

$ ./a2rchery.py import -h
usage: a2rchery import [-h] file

Import JSON file to update metadata in a .a2r disk image

positional arguments:
  file        .a2r disk image

optional arguments:
  -h, --help  show this help message and exit
```
