Translation Tools
======

How to add Translation Tools & extra translatable packages
------

In your root source folder:

    curl https://raw.github.com/DelphinPETER/TranslationTools/cm-10.1/repo_file/TranslationTools.xml > .repo/local_manifests/TranslationTools.xml
    repo sync

When the sync is finished, you can find Translation Tools under SOURCE_FOLDER/tools/TranslationTools/binary

If you want to get all the available CyanogenMod translatable packages that are not synced by default (not included in the default CM manifest), execute:

    curl https://raw.github.com/DelphinPETER/TranslationTools/cm-10.1/repo_file/cm_translations.xml > .repo/local_manifests/cm_translations.xml
    repo sync

Hint: if you are already downloaded some device repositories with "breakfast" and have problems syncing, execute:

    rm .repo/local_manifests/roomservice.xml
    repo sync
    breakfast <device>
    
Packages needed to be installed on your system
------

You need to have this packages installed on your system:

    sudo apt-get install libqt4-gui libqt4-xml libqt4-core
    
Script for quick access to Translation Tools
------
You can add [**tt script**](https://github.com/jackmu95/tt) for quick access to Translation Tools :

How to remove Translation Tools & extra translatable packages
-----

Remove Translation Tools:

    rm .repo/local_manifests/TranslationTools.xml
    repo sync

Remove extra packages:

    rm .repo/local_manifests/cm_translations.xml
    repo sync
