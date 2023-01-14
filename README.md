# *bsc-snapshots*


*\> [geth-snapshots](#geth-snapshots)*

**This geth snapshot is generated with `--tries-verify-mode=none` so it contains no MPT data. You should not build a validator upon this snapshot. [Know more >>>](https://github.com/bnb-chain/bsc/pull/926)**

*\> [erigon-snapshots](#erigon-snapshots)*

Updated every ~24~ 36 hours

Old snapshot deleted ~1~ 12 hours after new snapshot generated

## geth-snapshots


> Database uses [geth(v1.1.18)](https://github.com/bnb-chain/bsc/releases/tag/v1.1.18) for sync


### download

<!-- begin_geth -->

!!! from block [24761776](https://bscscan.com/block/24761776)

#### pipeline download and extract
> skip checksum & uncompress if you used pipeline
```bash
wget https://snapshots.48.club/geth.24761776.tar.lz4 -O - | lz4 -cd | tar xf -
```

#### multithreaded download

```bash
aria2c -s14 -x14 -k100M https://snapshots.48.club/geth.24761776.tar.lz4 -o geth.tar.lz4
```


### checksum

!!! db size 335.95 gb, 342.33 gb after decompression
```bash
> openssl sha256 geth.tar.lz4
SHA256(geth.tar.lz4)= 743dd866fda90f51caeaaf39378926663a2974182ad7c27be0ea66dd685fbf25
```

<!-- end_geth -->

### uncompress


running a script: _`lz4 -cd geth.tar.lz4 | tar xf -`_


### flags


```bash
--txlookuplimit=0 --syncmode=full --tries-verify-mode=none --pruneancient=true --diffblock=5000
```


## erigon-snapshots


> Database uses [erigon(v2.31.0-rc.2)](https://github.com/ledgerwatch/erigon/releases/tag/v2.31.0-rc.2) for sync


### download

<!-- begin_erigon -->

!!! from block [24717957](https://bscscan.com/block/24717957)

#### pipeline download and extract
> skip checksum & uncompress if you used pipeline
```bash
wget https://snapshots.48.club/erigon.24717957.tar.lz4 -O - | lz4 -cd | tar xf -
```

#### multithreaded download

```bash
aria2c -s14 -x14 -k100M https://snapshots.48.club/erigon.24717957.tar.lz4 -o erigon.tar.lz4
```


### checksum

!!! db size 961.75 gb, 1446.55 gb after decompression
```bash
> openssl sha256 erigon.tar.lz4
SHA256(erigon.tar.lz4)= c75a46a471f2d2845620bad94a190e85ddb01f894e66601730de28284b8d052b
```

<!-- end_erigon -->


### uncompress


running a script: _`lz4 -cd erigon.tar.lz4 | tar xf -`_


### flags


```bash
--chain=bsc --prune=hrtc --db.pagesize=16k
```
