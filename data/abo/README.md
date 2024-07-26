The ABO dataset can be downloaded from https://amazon-berkeley-objects.s3.amazonaws.com/index.html

For use with the SSTK, you will need to download the [abo-3dmodels.tar](https://amazon-berkeley-objects.s3.amazonaws.com/archives/abo-3dmodels.tar) file (154 GB).

Untar it and place it under `${ABO_ROOT}` together with the metadata files from this directory.
After untarring the `abo-3dmodels.tar`, make sure to gunzip `3dmodels/metadata/3dmodels.csv.gz`  
```
cd ${ABO_ROOT}
tar -xvf abo-3dmodels.tar
cd 3dmodels/metadata
gunzip 3dmodels.csv.gz
```

Copy metadata files in this directory into `${ABO_ROOT}`.

The directory structure should be:
```
${ABO_ROOT}
|-- 3dmodels                 - Untar of abo-3dmodels.tar
    |-- original             - GLBs from abo-3dmodels.tar
    |-- metadata             - metadata from abo-3dmodels.tar
        |-- 3dmodels.csv     - CSV file of 3dmodels
|-- abo.models.metadata.json - metadata for hooking up ABO object assets
```


To use these assets with the SmartScenes Toolkit (SSTK), 
```
# symlink `${ABO_ROOT}` to `${SSTK}/server/static/data/abo`
ln -s ${ABO_ROOT} ${SSTK}/server/static/data/abo
```

