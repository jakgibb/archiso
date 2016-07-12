Modified version of djgera's build scripts for my personal use (doubt these changes will help you).

build.sh modified to allow:

Alternative cache location:

    My archiso build system is booted to RAM and the build directory is located on an external HDD.
    As booting the system to RAM, this means my disk (located in RAM) is limited to the free RAM %.
    Set the cache directory to be a 'tmp' directory the build scripts location on a HDD.
    This may differ depending on where the external HDD is mounted, so modified build.sh to accomdate the changing mount point.
  
Removed 'run_once' from various functions:

    Allows adding/updating files from airootfs to the work directory and building a new ISO without having to run the entire build script process.
