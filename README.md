# AFRL Generator Cores
### Generators for various pre build needs
---

   author: Jay Convertino  
   
   date: 2022.08.09  
   
   details: Various generators for fusesoc cores, such as rom generators and software library handling.  
   
   license: MIT   
   
---

### Version
#### Current
  - V1.0.0 - initial release

#### Previous
  - none

### CORES

#### strromgen
  - interpreter: python3
  - command: python/strromgen.py
  - description: Generate ROMS based on YAML file containing strings and values.
  - usage: Bunch of cool stuff and such.
  - Parameters:
      - yaml_file   (str):  input file name to generate rom from in YAML format.
      - rom_file    (str):  output rom file name for binary contents.
      - endian      (str):  Endianess of integers.
      - num_bytes   (int):  Number of bytes for integer values.
      - string_size (int):  Number of characters for strings, including null terminator. All added characters will be null terminator.

#### vpilibmake
  - interpreter: python3
  - command: python/vpilibmake.py
  - description: Generate C libraries for VPI source code using make files.
  - usage: Bunch of cool stuff and such.
  - Parameters:
      - src_dirs (str): Directories containing the makefile for a library to build.

#### vpilibcmake
  - interpreter: python3
  - command: python/vpilibcmake.py
  - description: Generate C libraries for VPI source code using cmake files.
  - usage: Bunch of cool stuff and such.
  - Parameters:
      - src_dirs (str): Directories containing the cmake file for a library to build.
      - build_dir(str): Where to build output products. This defaults to build.
      - cmake_args(str): Arguments added to cmake build.

#### git_pull
  - interpreter: python3
  - command: python/git_pull.py
  - description: Pull git repos
  - usage: Bunch of cool stuff and such.
  - Parameters:
      - repo_url (str): URL where the git repo resides.
      - repo_dir (str): folder to put the pull.
      - tag (str): tag to checkout from pull.

##### Python Dependencies
  - PyYAML
  - GitPython

