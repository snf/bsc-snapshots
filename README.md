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
| Version | [v1.4.5](https://github.com/bnb-chain/bsc/releases/tag/v1.4.5) |
| Block | [38272690](https://bscscan.com/block/38272690) (Apr-29-2024 03:12:04 AM +UTC) |
| Link | `https://snapshots.48.club/geth.pbss.38272690.tar.zst` |
| Size | 832.64G <-> 911.51G |
| SHA256 | `53b128c100e56ed39467eaca9be5117778cf539260f445cd3c103a03e112d460` |
| Flags | `--history.transactions=0 --syncmode=full --db.engine=pebble --state.scheme=path` |
| Disk Suggestion | Minimum(NVMe ≥ 1T), Suggestion(NVMe ≥ 2T)|

[Back to TOC](#bsc-snapshots)

### Geth fast node

| Field |Value |
| --- | --- |
| Version | [v1.4.5](https://github.com/bnb-chain/bsc/releases/tag/v1.4.5) (https://github.com/bnb-chain/bsc/issues/2437) |
| Block | [38572390](https://bscscan.com/block/38572390) (May-09-2024 01:26:09 PM +UTC) |
| Link | `https://snapshots.48.club/geth.fast.38572390.tar.zst` |
| Size | 228.05G <-> 242.12G |
| SHA256 | `ba3211f02688467d615890be57c453dd641d1d328538a3a98ecc505b8215e48a` |
| Flags | `--history.transactions=0 --syncmode=full --db.engine=pebble --tries-verify-mode=none` |
| Disk Suggestion | Minimum(NVMe ≥ 300G), Suggestion(NVMe ≥ 1T)|

[Back to TOC](#bsc-snapshots)

### Geth full node

| Field |Value |
| --- | --- |
| Version | [v1.4.5](https://github.com/bnb-chain/bsc/releases/tag/v1.4.5) (https://github.com/bnb-chain/bsc/issues/2437) |
| Block | [38625976](https://bscscan.com/block/38625976) (May-11-2024 10:11:48 AM +UTC) |
| Link | `https://snapshots.48.club/geth.full.38625976.tar.zst` |
| Size | 738.14G <-> 814.19G |
| SHA256 | `749b057ddebd4ec93aaed2bb3ee60eee1c81147b3a57fc538f61f24c1deb1b5d` |
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
