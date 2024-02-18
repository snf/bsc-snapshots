# *bsc-snapshots*


- *[Geth](#geth)*
    - *[Geth full node with pbss](#geth-full-node-with-pbss)*
    - *[Geth fast node](#geth-fast-node)*
    - *[Geth full node](#geth-full-node)*
- *[How to download](#how-to-download)*
    - *[pipeline download and extract](#pipeline-download-and-extract)*
    - *[multithreaded download](#multithreaded-download)*

## Geth
### Geth full node with pbss

| Field |Value |
| --- | --- |
| Version | [v1.3.8](https://github.com/bnb-chain/bsc/releases/tag/v1.3.8) |
| Block | [35862472](https://bscscan.com/block/36229722) (Feb-18-2024 01:13:09 AM +UTC) |
| Link | `https://snapshots.48.club/geth.pbss.36229722.tar.zst` |
| Size | 799.85G <-> 874.86G |
| SHA256 | `a4469ecd723d6ee8382d6f12093f93ee77c83714fba22ee21beed72f66380fe8` |
| Flags | `--history.transactions=0 --syncmode=full --db.engine=pebble --state.scheme=path` |
| Disk Suggestion | Minimum(NVMe ≥ 1T), Suggestion(NVMe ≥ 2T)|

[Back to TOC](#bsc-snapshots)

### Geth fast node

| Field |Value |
| --- | --- |
| Version | [v1.3.7](https://github.com/bnb-chain/bsc/releases/tag/v1.3.7) |
| Block | [35407303](https://bscscan.com/block/35407303) (Jan-20-2024 10:27:11 AM +UTC) |
| Link | `https://snapshots.48.club/geth.fast.35407303.tar.zst` |
| Size | 367.24G <-> 419.32G |
| SHA256 | `b3d562b9c2c64b22475b9af93ade57b0d3c978a625205a9321e313781e169d7a` |
| Flags | `--history.transactions=0 --syncmode=full --tries-verify-mode=none --pruneancient --db.engine=pebble` |
| Disk Suggestion | Minimum(NVMe ≥ 500G), Suggestion(NVMe ≥ 1T)|

[Back to TOC](#bsc-snapshots)

### Geth full node

| Field |Value |
| --- | --- |
| Version | [v1.3.8](https://github.com/bnb-chain/bsc/releases/tag/v1.3.8) |
| Block | [35956781](https://bscscan.com/block/35956781) (Feb-08-2024 01:19:46 PM +UTC) |
| Link | `https://snapshots.48.club/geth.full.35956781.tar.zst` |
| Size | 666.12G <-> 736.72G |
| SHA256 | `45a1ad3ee04d112ecbd75e617ee78213e39d0434e233944668003e1d9706218b` |
| Flags | `--history.transactions=0 --syncmode=full --db.engine=pebble` |
| Disk Suggestion | Minimum(NVMe ≥ 1T), Suggestion(NVMe ≥ 3T)|

[Back to TOC](#bsc-snapshots)

## How to download
### pipeline download and extract

```bash
wget $Link -O - | zstd -cd | tar xf -
```

### multithreaded download

```bash
aria2c -s4 -x4 -k1024M $Link -o $save_path
zstd -cd $save_path | tar xf -
openssl sha256 $save_path # checksum verification, optional
```

[Back to TOC](#bsc-snapshots)
