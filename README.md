# TWRP for Mi A3
## How to compile:
1. Install the [building dependencies](https://github.com/akhilnarang/scripts).

2. Execute the following command to initialize a minimal TWRP repository with a shallow clone:

```bash
repo init -u git://github.com/minimal-manifest-twrp/platform_manifest_twrp_omni.git -b twrp-9.0 --depth=1
```

3. Then, to sync up:

```bash
repo sync
```

4. Now clone the device tree:

```bash
git clone https://github.com/maffeen/device_xiaomi_laurel_sprout-twrp device/xiaomi/laurel_sprout
```

5. Lastly, run these commands to build the TWRP:

```bash
. build/envsetup.sh; lunch omni_laurel_sprout-eng; mka bootimage
```
