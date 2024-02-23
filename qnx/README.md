# Compile the port for QNX

**Note**: QNX ports areo only supported from a **Linux host** operating system

### Clone repository

    git clone git@gitlab.rim.net:qnx/osr/abseil-cpp

### Checkout corresponding SDP branch

    git checkout qnx-sdp8-master

or

    git checkout qnx-sdp71-master

### Setup QNX SDP environment

    source <path-to-sdp>/qnxsdp-env.sh

### Build

- From the root folder, type:
  - `OSLIST=nto make -C qnx/build install`
