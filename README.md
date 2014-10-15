AOSPA Legacy (WIP)
================

By SaberMod and AOSPAL.
This is the AOSP/Nexus GitHub. For Legacy (non-Nexus), please [click here](https://github.com/SaberDroid-Legacy).


Optimizations (WIP):
--------------------

 * -O3
 * strict-aliasing (level 3)
 * odex and deodex builds
 * SaberMod GCC 4.9.Y+ (kernel)
 * SaberMod GCC 4.8.Y+ (ROM)
 * SaberMod GCC 4.8/4.9+ (host)
 * modular implemented via vendor
 * Graphite
 * pthread
 * gold LD


How to sync and build:
----------------------
### Initialize and Sync: ###

    repo init -u git://github.com/h2o64/manifest.git -b AOSPA_LINARO
    repo sync -j<#>

### Build (manually): ###
    . build/envsetup.sh
    lunch
    make -j<#>
    
### Build (autmoatically): ###
    ./build.sh <DEVICE>

### Legend: ###
    <DEVICE> = codename of the desired device you would like to build
    <BRANCH> = branch you want to use (i.e: kitkat)
    <#>      = number of threads or jobs you wish to use for syncing or building
               CAUTION: higher threads on sync will take up more bandwidth
                        & higher threads on build will use more CPU power!
