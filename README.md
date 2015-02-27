How to compile your own mk/unpackbootimg, mkbootfs binary
---------------------------------------------------------

This is a very simple task and takes less then a minute. Simple run :

    $ git clone https://github.com/CyanogenMod/android_system_core -b cm-12.0
    $ cd android_system_core
    $ gcc -o ~/mkbootimg libmincrypt/*.c mkbootimg/mkbootimg.c -Iinclude
    $ gcc -o ~/unpackbootimg libmincrypt/*.c mkbootimg/unpackbootimg.c -Iinclude
    $ gcc -o ~/mkbootfs libmincrypt/*.c cpio/mkbootfs.c -Iinclude

The binaries have now been created in your home directory, go and check them out. If you want to repeat this process run :

    $ cd android_system_core
    $ git pull
    $ gcc -o ~/mkbootimg libmincrypt/*.c mkbootimg/mkbootimg.c -Iinclude
    $ gcc -o ~/unpackbootimg libmincrypt/*.c mkbootimg/unpackbootimg.c -Iinclude
    $ gcc -o ~/mkbootfs libmincrypt/*.c cpio/mkbootfs.c -Iinclude
