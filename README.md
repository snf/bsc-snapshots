# *bsc-snapshots*


*\> [geth-snapshots](#geth-snapshots)*

*\> [erigon-snapshots](#erigon-snapshots)*


## geth-snapshots


> Database uses [geth(v1.1.11)](https://github.com/bnb-chain/bsc/releases/tag/v1.1.11) for sync


### download

<!-- begin_geth -->

!!! from block [19564171](https://bscscan.com/block/19564171)
```bash
aria2c -s14 -x14 -k100M https://snapshots.bnb48.club/geth.19564171.tar.lz4 -o geth.tar.lz4
```


### checksum


!!! db size 546.19 gb, 558.29 gb after decompression
```bash
> openssl sha256 geth.tar.lz4
SHA256(geth.tar.lz4)= f1301289efc2653a2447180fc54a0c7dc2823fb8c2b3343d0bc17dc94866cb53
```

<!-- end_geth -->

### uncompress


running a script: _`lz4 -cd geth.tar.lz4 | tar xf -`_


### flags


```bash
--txlookuplimit=0 --diffsync --syncmode=snap
```


## erigon-snapshots


> Database uses [erigon(v2022.07.02)](https://github.com/ledgerwatch/erigon/releases/tag/v2022.07.02) for sync


### download

<!-- begin_erigon -->

!!! from block [19590525](https://bscscan.com/block/19590525)
```bash
aria2c -s14 -x14 -k100M https://snapshots.bnb48.club/erigon.19590525.tar.lz4 -o erigon.tar.lz4
```


### checksum


!!! db size 755.58 gb, 1073.51 gb after decompression
```bash
> openssl sha256 erigon.tar.lz4
SHA256(erigon.tar.lz4)= 24afd86abb83d517f5e6df688f103f85f2a790800910c565d9d2aca170224155
```

<!-- end_erigon -->

### uncompress


running a script: _`lz4 -cd erigon.tar.lz4 | tar xf -`_


### flags


```bash
--chain=bsc --prune= --prune.h.older=5000 --prune.r.older=5000 --prune.t.older=5000 --prune.c.older=5000 --db.pagesize=16k
```
