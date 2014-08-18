android_local_h2o64
===================

Local Manifest for Ubuntu Touch 14.10 (phablet-4.4.2_r1)

Getting Started
---------------

To get started with Android, you'll need to get
familiar with [Git and Repo](http://source.android.com/download/using-repo).

Make a build directory:

	mkdir Ubuntu_Touch (or whatever name you choose)
	cd Ubuntu_Touch (or the name  you chose)
	mkdir .repo/local_manifests

To initialize your local repository using the CyanogenMod manifest, use commands like these:

    repo init -u https://code-review.phablet.ubuntu.com/p/aosp/platform/manifest.git -b phablet-4.4.2_r1

    curl -L -o .repo/local_manifests/roomservice_CAF.xml -O -L https://raw.githubusercontent.com/h2o64/android_local_h2o64/phablet-4.4.2_r1-caf/roomservice_CAF.xml
 
    	( or Download: https://raw.githubusercontent.com/h2o64/android_local_h2o64/phablet-4.4.2_r1-caf/roomservice_CAF.xml
		and place it in ~/Ubuntu_Touch/.repo/local_manifest.xml (or ~/'name you chose'/.repo)

Then to sync up:

    repo sync

Let's build it

    . build/envsetup.sh

Choose the number for

    full_falcon-userdebug

Useally 17.
Start the building process (Take long time, depending from your computer)

    make -j4

MEMO (check the xda thread) : 
There is an error with gps.h
There is something to do with system/core/mkbootimg.
