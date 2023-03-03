# *bsc-snapshots*


*\> [geth-snapshots](#geth-snapshots)*

**This geth snapshot is generated with `--tries-verify-mode=none` so it contains no MPT data. You should not build a validator upon this snapshot. [Know more >>>](https://github.com/bnb-chain/bsc/pull/926)**

*\> [erigon-snapshots](#erigon-snapshots)*

Updated every ~24~ 36 hours

Old snapshot deleted ~1~ 12 hours after new snapshot generated

## geth-snapshots


> Database uses [geth(v1.1.19)](https://github.com/bnb-chain/bsc/releases/tag/v1.1.19) for sync


### download

<!-- begin_geth -->

!!! from block [26088082](https://bscscan.com/block/26088082)

#### pipeline download and extract
> skip checksum & uncompress if you used pipeline
```bash
wget https://snapshots.48.club/geth.26088082.tar.lz4 -O - | lz4 -cd | tar xf -
```

#### multithreaded download

```bash
aria2c -s14 -x14 -k100M https://snapshots.48.club/geth.26088082.tar.lz4 -o geth.tar.lz4
```


### checksum

!!! db size 352.02 gb, 358.78 gb after decompression
```bash
> openssl sha256 geth.tar.lz4
SHA256(geth.tar.lz4)= 2985f16e0cbea748575794251ae47be8dad01800c8d88f65dcb93e6c24847156
```

<!-- end_geth -->

### uncompress


running a script: _`lz4 -cd geth.tar.lz4 | tar xf -`_


### flags


```bash
--txlookuplimit=0 --syncmode=full --tries-verify-mode=none --pruneancient=true --diffblock=5000
```


## erigon-snapshots


> Database uses [erigon(v2.39.0)](https://github.com/ledgerwatch/erigon/releases/tag/v2.39.0) for sync


### download

<!-- begin_erigon -->

!!! from block [26086043](https://bscscan.com/block/26086043)

#### pipeline download and extract
> skip checksum & uncompress if you used pipeline
```bash
wget https://snapshots.48.club/erigon.26086043.tar.lz4 -O - | lz4 -cd | tar xf -
```

#### multithreaded download

```bash
aria2c -s14 -x14 -k100M https://snapshots.48.club/erigon.26086043.tar.lz4 -o erigon.tar.lz4
```


### checksum

!!! db size 1013.56 gb, 1520.54 gb after decompression
```bash
> openssl sha256 erigon.tar.lz4
SHA256(erigon.tar.lz4)= a50788267c11fdab3ca83655ab9d7a4f64db33b32e7c143bc46e647658ad8a98
```

<!-- end_erigon -->


### uncompress


running a script: _`lz4 -cd erigon.tar.lz4 | tar xf -`_


### flags


```bash
--chain=bsc --prune=hrtc --db.pagesize=16k
```
