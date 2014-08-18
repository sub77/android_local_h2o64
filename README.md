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

    curl -L -o .repo/local_manifests/msm8226.xml -O -L https://raw.github.com/razrqcom-dev-team/android_local_razrqcom/msm8226-kk/msm8226.xml
 
    	( or Download: https://github.com/razrqcom-dev-team/android_local_razrqcom/blob/msm8226-kk/msm8226.xml
		and place it in ~/Android/.repo/local_manifest.xml (or ~/'name you chose'/.repo)

Then to sync up:

    repo sync

TIPS : 
There is an error with gps.h
There is something to do with system/core/mkbootimg.
