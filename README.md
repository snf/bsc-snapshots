# *bsc-snapshots*


*\> [geth-snapshots](#geth-snapshots)*

*\> [erigon-snapshots](#erigon-snapshots)*

Updated every ~24~ 36 hours

Old snapshot deleted ~1~ 12 hours after new snapshot generated

## geth-snapshots


> Database uses [geth(v1.1.12)](https://github.com/bnb-chain/bsc/releases/tag/v1.1.12) for sync


### download

<!-- begin_geth -->

!!! from block [20005387](https://bscscan.com/block/20005387)
```bash
aria2c -s14 -x14 -k100M https://snapshots.bnb48.club/geth.20005387.tar.lz4 -o geth.tar.lz4
```


### checksum


!!! db size 554.35 gb, 566.15 gb after decompression
```bash
> openssl sha256 geth.tar.lz4
SHA256(geth.tar.lz4)= ed7e10aa9b6b645f4bc023fedd57b108e50642265d03a61aba69a163d48ec179
```

<!-- end_geth -->

### uncompress


running a script: _`lz4 -cd geth.tar.lz4 | tar xf -`_


### flags


```bash
--txlookuplimit=0 --diffsync=true --syncmode=full --tries-verify-mode=none --pruneancient=true --diffblock=5000
```


## erigon-snapshots


> Database uses [erigon(v2022.07.04)](https://github.com/ledgerwatch/erigon/releases/tag/v2022.07.04) for sync


### download

<!-- begin_erigon -->

!!! from block [20046900](https://bscscan.com/block/20046900)
```bash
aria2c -s14 -x14 -k100M https://snapshots.bnb48.club/erigon.20046900.tar.lz4 -o erigon.tar.lz4
```


### checksum


!!! db size 753.74 gb, 1077.33 gb after decompression
```bash
> openssl sha256 erigon.tar.lz4
SHA256(erigon.tar.lz4)= c4a8d3e5c1e8bb3f693bfed03bf928125a8d17064549af3ebfa404d500a94349
```

<!-- end_erigon -->

### uncompress


running a script: _`lz4 -cd erigon.tar.lz4 | tar xf -`_


### flags


```bash
--chain=bsc --prune= --prune.h.older=5000 --prune.r.older=5000 --prune.t.older=5000 --prune.c.older=5000 --db.pagesize=16k
```
