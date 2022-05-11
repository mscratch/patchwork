core_analyzer-d057d4d-tcmalloc-3level-pgtbl.patch
-------------------------------------------------

The patch contains the support of TCMalloc 2.7+, when built with macro `TCMALLOC_SMALL_BUT_SLOW` defined.

This macro enables TCMalloc to use 3 level page table, to reduce the memory size while suffering some performance.

Links:

* <https://github.com/yanqi27/core_analyzer>

## Building

You should change the `build_gdb.sh` in `core_analyzer`'s repository, like:

```shell
cd $gdb_to_install
cp -rLv $PROJECT_FOLDER/gdbplus/gdb-9.2/gdb .
# add this line!
mv -fv gdb/Makefile.in{.tcmalloc,}
```

then run the script to build directly.
