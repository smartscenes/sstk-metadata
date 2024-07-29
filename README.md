# metadata
SmartScenes metadata files to hookup supported assets with the [SSTK](https://github.com/smartscenes/sstk)

To hookup the metadata to the SSTK, follow the instructions in the respective READMEs for each asset type
and add the appropriate metadata files to:
- [${STK}/server/static/data/assets-extra.json](https://github.com/smartscenes/sstk/blob/master/server/static/data/assets-extra.json) for use with SSTK webapp
- [${STK}/server/ssc/data/assets.json](https://github.com/smartscenes/sstk/blob/master/ssc/data/assets.json) for use with SSTK headless rendering (the SSC scripts)

To each `assets.json` file, add the following:
```
  {
    "name": <dataset-name>,
    "type": <model|scan|scene>,            # asset type (use "model" for simple mesh, "scan" for scanned mesh, "scene" for composition of 3D assets)
    "metadata": <path to metadata>,
    "ids": <path to CSV with ID>           # omit if using solr to search
  }
```

As an example, below is the entry for the NYUv2 dataset in [${STK}/server/static/data/assets-extra.json](https://github.com/smartscenes/sstk/blob/master/server/static/data/assets-extra.json).  
```
  {
    "name": "nyuv2",
    "type": "scan", 
    "metadata": "${assetsDir}/data/scannet/nyuv2.json",
    "ids": "${assetsDir}/data/scannet/nyuv2.csv"
  }
```
For the webapp, `${assetsDir}` goes to path that the server is running on (e.g. http://localhost:8010/resources).   For the SSC [${STK}/server/ssc/data/assets.json](https://github.com/smartscenes/sstk/blob/master/ssc/data/assets.json), the path can be specified relative to the location of the json file (e.g. `../server/static/data/matterport/mpr3d.csv`).

See [SSTK wiki on how to prepare assets](https://github.com/smartscenes/sstk/wiki/Preparing-assets-for-annotation) for more information.

## Supported dataset metadata summary

| metadata | Dataset       | Type       | Size |
| ------------- |:-------------:|:-------------:| -----:|
| metadata | Dataset       | Type       | Size |
| ------------- |:-------------:|:-------------:| -----:|
| [v0.5.3](data/shapenet) | [ShapeNet](www.shapenet.org)  | 3D models | Large dataset of 3D models |
| [v0.5.4](data/abo) | [ABO](https://amazon-berkeley-objects.s3.amazonaws.com/index.html)  | 3D models | Large dataset of ~8K 3D models |
| Coming soon |  [Stanford Scene Database](http://graphics.stanford.edu/projects/scenesynth/)    | Synthetic scenes      |  150 rooms |
| [v0.5.4](data/hssd) | [HSSD](https://3dlg-hcvc.github.io/hssd/) | Synthetic Scenes       |    211 houses, ~18K 3D models |
| [v0.5.4](data/3dfront) | [3DFront](https://tianchi.aliyun.com/specials/promotion/alibaba-3d-scene-dataset) | Synthetic Scenes       |    1.9K houses with objects from [3DFuture](https://tianchi.aliyun.com/specials/promotion/alibaba-3d-future) |
| [v0.5.4](data/structured3d) | [Structured3D](https://structured3d-dataset.org/) | Synthetic Architecture      |    3.5K house layouts |
| [v0.5.1](data/scannet) | [ScanNet](http://www.scan-net.org/)  | Reconstructions      | ~1500 scans of ~700 regions and rooms |
| [v0.5.1](data/nyuv2) | [NYUv2](https://cs.nyu.edu/~silberman/datasets/nyu_depth_v2.html)  | Reconstructions      | ~500 scans |
| [v0.5.1](data/matterport) | [Matterport3D](https://github.com/niessner/Matterport) | Reconstructions      |    90 houses with over 2000 regions |
| [v0.5.1](data/scenenn/) | [SceneNN](http://people.sutd.edu.sg/~saikit/projects/sceneNN/) | Reconstructions | |
| Coming soon | [2D-3D-S](http://buildingparser.stanford.edu/dataset.html) | Reconstructions | |

## Changelog

Refer to [CHANGELOG.md](CHANGELOG.md) for a record of notable changes.
