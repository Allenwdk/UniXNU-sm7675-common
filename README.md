# UniXNU SM7675 support

Shared Qualcomm SM7675 (cliffs) support for UniXNU: CPU topology, GICv3, UFS
and Adreno 732 resources, GMU operations, GPU SMMU integration, and XNU
patches.

`soc.toml` selects `Adreno740` and `AdrenoMetal` as the default GPU stack;
device repositories refine the selection (the uke board runs the A732-capable
Adreno fork) and supply memory layout, peripherals, firmware, power policy,
and packaging.

Hardware descriptions derive from the uke vendor_boot device tree and the
Xiaomi kernel sources at revision `5712080a4b0c0b1a879e6d145c601c649ddaddfd`
of [Xiaomi_Kernel_OpenSource](https://github.com/MiCode/Xiaomi_Kernel_OpenSource).

Build through the [UniXNU CLI](https://unixnu.com/building).
Read the [device repository specification](https://unixnu.com/porting/device-repository),
[device-tree specification](https://unixnu.com/porting/device-tree),
and [component catalog](https://unixnu.com/reference/components).

## Contents

| Path | Contents |
| --- | --- |
| `soc.toml` | SoC profile and component selection |
| `configs/` | Kernel configuration fragments |
| `dts/sm7675.dtsi` | Shared hardware resources |
| `patches/xnu/series` | Ordered SoC patches |


## Uke GPU27 integration (2026-11-03)

This SoC implementation is part of the user-accepted uke iPadOS27/24A446 GPU baseline, kernel CRC `90B6BC701210D9DB`. Shared GMU and SMMU operations support the board-provided gen7_11_0 firmware/windows and OPP policy. The user confirms prior boot, icons/widgets and Settings/Dock UI-restart symptoms resolved. Detailed image identities and scope belong to the device repository; long-run stress remains unmeasured.
