# android_device_huawei_hi3660

Common Kirin 960 (`hi3660`) device tree adapted from `Huawei-Dev/android_device_huawei_hi3660` (`android@13`) for clean **AOSP 13** builds on **HUAWEI MediaPad M5 (`CMR-W09`)**.

## AOSP 13 Adaptations

- Dropped LineageOS HAL dependencies (`livedisplay@2.1`, `touch@1.0`, `trust@1.0`, `overlay-lineage`) and fixed `sepolicy` / `hwservice_contexts` for AOSP 13 (`hi3660-aosp.patch`).
- Tuned `powerhint.json` and `vendor.prop` for 60Hz SurfaceFlinger and HWUI rendering (`hi3660-perf-and-charger.patch`).
- Added 256 MB `system_ext` headroom for MindTheGapps 13 (`hi3660-system-ext-size.patch`) and trimmed trailing NUL in `init_hisi` properties (`hi3660-init-nul-trim.patch`).
- Full build pipeline and product configuration live in [`SuspectWorkers/aosp13-m5`](https://github.com/SuspectWorkers/aosp13-m5).
