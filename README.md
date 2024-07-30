# Musepack .MPC Encoder (mpcenc) Windows artifacts for all interesting architectures
Here you can find builds of mpcenc to convert music files to the "Musepack" format, for all architectures of Windows !
Since I could not find builds for all architectures of Windows (especially ARM64), I decided to tinker myself to compile the source code of Musepack under a modern Visual Studio 2022 environment.

You can find the whole source code here : https://www.musepack.net/index.php?pg=src
The version of mpcenc provided here comes from the sources of the r475 (providing this info for reference, just in case the musepack team decides to create new updates in the future even if it is probably very unlikely).

# How to use it ?
I recommend using it through Foobar2000 because Foobar2000 is good at handling tags and at multi-threading the encoding process to use all cores of your CPU to speed up the whole process as much as possible.
If you are on the ARM64 architecture, use the ARM64 build to get the best performance.
If you are on the INTEL64 architecture, you may try the INTEL64 build to get a slight improvement in encoding performance.

Just copy/paste/replace it here : C:\Program Files\foobar2000\encoders

Then configure Foobar2000 normally and it will use it. If you are on ARM64, you should see a very very big encoding performance improvement (up to 2.5x).

# Why not use the build of mpcenc (Musepack encoder) provided by default by Foobar2000 ?
It's compiled for Intel x86 and for some reason ARM64 Windows 11 (and even CrossOver/Wine directly on MacOS/Linux) is struggling hard with it. Using a native ARM64 binary is just much faster.

# Enjoy !