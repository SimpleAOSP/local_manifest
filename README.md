
To build SimpleAOSP, sync AOSP using
```bash
mkdir SAOSP && cd SAOSP
repo init -u https://android.googlesource.com/platform/manifest -b android-15.0.0_r1 --depth 1
git clone https://github.com/SimpleAOSP/local_manifest .repo/local_manifests
repo sync -j$(nproc --all)
```

To build (Replace devicename with your synced device tree codenames)

```bash
lunch aosp_devicename-ap3a-user
m updatepackage
```

Your build should be available in `out/target/product/devicename/`
