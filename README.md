# *bsc-snapshots*


- *[Geth](#geth)*
    - *[Geth fast node with pbss](#geth-fast-node-with-pbss)*
    - *[Geth full node with pbss](#geth-full-node-with-pbss)*
    - *[Geth fast node](#geth-fast-node)*
    - *[Geth full node](#geth-full-node)*
- *[How to download](#how-to-download)*
    - *[pipeline download and extract](#pipeline-download-and-extract)*
    - *[multithreaded download](#multithreaded-download)*

## Geth
### Geth fast node with pbss

| Field |Value |
| --- | --- |
| Version | [v1.4.8](https://github.com/bnb-chain/bsc/releases/tag/v1.4.8) |
| Block | [39221903](https://bscscan.com/block/39221903) (Jun-01-2024 04:00:57 AM +UTC) |
| Link | `https://snapshots.48.club/pbss.fast.39221903.tar.zst` |
| Size | 306.68G <-> 337.79G |
| SHA256 | `e5a7a8e7d5693abcb7b12f175d5e7c26501b905947a141e5b971849807de1ba6` |
| Flags | `--history.transactions=90000 --syncmode=full --db.engine=pebble --tries-verify-mode=none` |
| Disk Suggestion | Minimum(NVMe ≥ 500G), Suggestion(NVMe ≥ 1T)|

[Back to TOC](#bsc-snapshots)

### Geth full node with pbss

| Field |Value |
| --- | --- |
| Version | [v1.4.6](https://github.com/bnb-chain/bsc/releases/tag/v1.4.6) |
| Block | [38774285](https://bscscan.com/block/38774285) (May-16-2024 02:04:13 PM +UTC) |
| Link | `https://snapshots.48.club/geth.pbss.38774285.tar.zst` |
| Size | 833.44G <-> 910.35G |
| SHA256 | `fb69243816383c86b99a818075ad4ee4faeec2e8ac51800ee0df0aabc3337bba` |
| Flags | `--history.transactions=90000 --syncmode=full --db.engine=pebble` |
| Disk Suggestion | Minimum(NVMe ≥ 1T), Suggestion(NVMe ≥ 2T)|

[Back to TOC](#bsc-snapshots)

### Geth fast node

| Field |Value |
| --- | --- |
| Version | [v1.4.8](https://github.com/bnb-chain/bsc/releases/tag/v1.4.8) |
| Block | [39000831](https://bscscan.com/block/39000831) (May-24-2024 11:17:08 AM +UTC) |
| Link | `https://snapshots.48.club/geth.fast.39000831.tar.zst` |
| Size | 229.16G <-> 240.91G |
| SHA256 | `9ddc64dc30566a7afaf99b6ceb35c3d99cc07e1555b2e8fc155fefcaa2ef5fcc` |
| Flags | `--history.transactions=90000 --syncmode=full --db.engine=pebble --tries-verify-mode=none` |
| Disk Suggestion | Minimum(NVMe ≥ 300G), Suggestion(NVMe ≥ 1T)|

[Back to TOC](#bsc-snapshots)

### Geth full node

| Field |Value |
| --- | --- |
| Version | [v1.4.6](https://github.com/bnb-chain/bsc/releases/tag/v1.4.6) |
| Block | [38767853](https://bscscan.com/block/38767853) (May-16-2024 08:42:11 AM +UTC) |
| Link | `https://snapshots.48.club/geth.full.38767853.tar.zst` |
| Size | 728.72G <-> 804.72G |
| SHA256 | `91c6ee60aa681d929720f342f2a47a910de2e2ea7f7c4424fc7944c7a5d2ceb5` |
| Flags | `--history.transactions=90000 --syncmode=full --db.engine=pebble` |
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
