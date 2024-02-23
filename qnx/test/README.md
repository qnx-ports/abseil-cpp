# Testing abseil-cpp on QNX

Compile abseil-cpp for desired architecture under qnx/build using `JLEVEL=4 make install`

**RPI4**: Move abseil-cpp library and the test binary to the target:

e.g.

    - scp ~/abseil-cpp/qnx/build/nto-aarch64-le/build/bin/* root<target-ip-address>:/usr/bin
    - scp ~/abseil-cpp/qnx/build/nto-aarch64-le/build/lib* root@<target-ip-address>:/usr/lib

Make sure to find all libsabsl* libraries and copy them over to the target: installed under ~/qnx800_ea/target/qnx/aarch64le/usr/lib

ssh into target and run the binary.

In order to run all test binaries, you can copy over the qnxtests.sh file under the qnx/test folder and run the file instead.

**QEMU**: Move abseil library and test binary to qemu instance:

    - scp ~/abseil-cpp/qnx/build/nto-x86_64/build/bin/* root<target-ip-address>:/system/xbin
    - scp ~/abseil-cpp/qnx/build/nto-x86_64/build/lib/lib* root<target-ip-address>:/system/lib

---
Tests results are provided on the wiki: https://wikis.rim.net/display/OSG/QNX+Open+Source+Group