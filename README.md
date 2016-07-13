Modified version of djgera's build scripts.
These changes are to suite my personal needs, so they are unlikely to benefit you.

## build.sh modified to allow:

### Set alternative cache location:  
The original build script sets the cache directory to systems current cache directory with:  
`_cache_dirs=($(pacman -v 2>&1 | grep '^Cache Dirs:' | sed 's/Cache Dirs:\s*//g'))`
As my dedicated build system is booted to RAM and the work directory stored on an external drive, this will fill up the RAM filesystem.
The script has been modified to set the _cache_dir to where the work directory is currently mounted ('*currentWorkDirectory*/tmp'). The mount point can change so is not harcoded.

### Removed 'run_once' from two functions calls:  
Removed 'run_once' from 'make_prepare' and 'make_iso'.  
This allows adding/updating files from airootfs to the current build and creating a new ISO without having to run the entire build script process.

### Added package check option:  
Added a new flag, invoked with -p, which will check each package listed in the packages.* file actually exist in the repos.  
This prevents the build process from failing after run
