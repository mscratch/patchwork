make-4.3-mingw-output-clion.patch
---------------------------------

This patch contains what you need to build GNUmake 4.3 using MSYS2/MinGW64.

Besides, it adds a feature that translate MSYS path `/c/` into `c:/`, make CLion (and me) happy😀.

Links:
* <https://ftp.gnu.org/gnu/make/make-4.3.tar.gz>
* <https://github.com/msys2/MINGW-packages/tree/8302516/mingw-w64-make>

To Build:
1. Fetch the source using first link, and extract it blablabla.
2. Apply the patch.
3. Starting `MSYS2 MinGW 64-bit` terminal, go into the source directory.
4. Run `./build_w32.bat --without-guile gcc`.
5. That's all, you will find your binary at `./GccRel/gnumake.exe`

Lastly, you may want to configure the CLion to use the customized `gnumake.exe`.
