# Lineage buildscripts
========================

Please note, I use ~/lineage in this README but you can use whatever folder name you want.

Also please note that repopick.sh isn't always updated. Please check LineageOS Gerrit in case there is changes to repopick topics.

Starting from zero:
---------
    mkdir -p ~/lineage
    cd ~/ineage
    repo init -u git://github.com/LineageOS/android.git -b lineage-16.0
    mkdir -p .repo/local_manifests
    curl https://raw.githubusercontent.com/moto999999/local_manifests/lineage-16.0/local_manifest.xml > .repo/local_manifests/my_manifest.xml
    repo sync
    # OPTIONAL to use repopick unless you want to test WIP commits
    curl https://raw.githubusercontent.com/moto999999/local_manifests/lineage-16.0/repopick.sh > repopick.sh
    ./repopick.sh

If you've already synced Lineage-Sources:
----------
    mkdir -p .repo/local_manifests
    curl https://raw.githubusercontent.com/moto999999/local_manifests/lineage-16.0/local_manifest.xml > .repo/local_manifests/my_manifest.xml
    repo sync
    # OPTIONAL to use repopick unless you want to test WIP commits
    curl https://raw.githubusercontent.com/moto999999/local_manifests/lineage-16.0/repopick.sh > repopick.sh
    ./repopick.sh

Building
----------
    cd ~/lineage
    curl https://raw.githubusercontent.com/moto999999/local_manifests/lineage-16.0/clean-x10-build.sh > clean_x10_build.sh
    curl https://raw.githubusercontent.com/moto999999/local_manifests/lineage-16.0/dirty-x10-build.sh > dirty_x10_build.sh
    ./clean_x10_build.sh // for clean builds
    ./dirty_x10_build.sh // for dirty builds

I made these modified scripts for convenience plus logs terminal output to files for easy scrolling later in your favorite text editor.
