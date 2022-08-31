# *bsc-snapshots*


*\> [geth-snapshots](#geth-snapshots)*

*\> [erigon-snapshots](#erigon-snapshots)*

Updated every ~24~ 36 hours

Old snapshot deleted ~1~ 12 hours after new snapshot generated

## geth-snapshots


> Database uses [geth(v1.1.12)](https://github.com/bnb-chain/bsc/releases/tag/v1.1.12) for sync


### download

<!-- begin_geth -->

!!! from block [20806867](https://bscscan.com/block/20806867)
```bash
aria2c -s14 -x14 -k100M https://snapshots.bnb48.club/geth.20806867.tar.lz4 -o geth.tar.lz4
```


### checksum


!!! db size 570.13 gb, 582.43 gb after decompression
```bash
> openssl sha256 geth.tar.lz4
SHA256(geth.tar.lz4)= de94ea55ecdcde01c25aefe24fffe59ec473bf41c9ad3d47fdd1acc773ba96ec
```

<!-- end_geth -->

### uncompress


running a script: _`lz4 -cd geth.tar.lz4 | tar xf -`_


### flags


```bash
--txlookuplimit=0 --diffsync=true --syncmode=full --tries-verify-mode=none --pruneancient=true --diffblock=5000
```


## erigon-snapshots


> Database uses [erigon(v2022.08.03)](https://github.com/ledgerwatch/erigon/releases/tag/v2022.08.03) for sync


### download

<!-- begin_erigon -->

!!! from block [20926497](https://bscscan.com/block/20926497)
```bash
aria2c -s14 -x14 -k100M https://snapshots.bnb48.club/erigon.20926497.tar.lz4 -o erigon.tar.lz4
```


### checksum


!!! db size 818.75 gb, 1191.11 gb after decompression
```bash
> openssl sha256 erigon.tar.lz4
SHA256(erigon.tar.lz4)= 161236aa78a343b63e213f5d19ad1f4f609bd692114aa2b59df39633ce672f40
```

<!-- end_erigon -->

### uncompress


running a script: _`lz4 -cd erigon.tar.lz4 | tar xf -`_


### flags


```bash
--chain=bsc --prune=hrtc --db.pagesize=16k
```
