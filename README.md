# metadata
SmartScenes metadata files to hookup supported assets with the [SSTK](https://github.com/smartscenes/sstk)

To hookup the metadata to the SSTK, follow the instructions in the respective READMEs for each asset type
and add the appropriate metadata files to:
- [${STK}/server/static/data/assets-extra.json](https://github.com/smartscenes/sstk/blob/master/server/static/data/assets-extra.json) for use with SSTK webapp
- [${STK}/server/ssc/data/assets.json](https://github.com/smartscenes/sstk/blob/master/ssc/data/assets.json) for use with SSTK headless rendering

See [SSTK wiki on how to prepare assets](https://github.com/smartscenes/sstk/wiki/Preparing-assets-for-annotation) for more information.

## Supported dataset metadata summary

| metadata | Dataset       | Type       | Size |
| ------------- |:-------------:|:-------------:| -----:|
| [v0.1](data/shapenet) | [ShapeNet](www.shapenet.org)  | 3D models | Large dataset of 3D models |
| Coming soon |  [Stanford Scene Database](http://graphics.stanford.edu/projects/scenesynth/)    | Synthetic scenes      |  150 rooms |
| [v0.1](data/suncg) | [SUNCG](suncg.cs.princeton.edu) | Synthetic Scenes      |    >45K houses, ~2000 models |
| [v0.1](data/scannet) | [ScanNet](http://www.scan-net.org/)  | Reconstructions      | ~1500 scans of ~700 regions and rooms |
| [v0.1](data/nyuv2) | [NYUv2](https://cs.nyu.edu/~silberman/datasets/nyu_depth_v2.html)  | Reconstructions      | ~500 scans |
| [v0.1](data/matterport) | [Matterport3D](https://github.com/niessner/Matterport) | Reconstructions      |    90 houses with over 2000 regions |
| [v0.1](data/structured3d) | [Structured3D](https://structured3d-dataset.org/) | Synthetic Scenes      |    3.5K house designs |
| Coming soon | [SceneNN](http://people.sutd.edu.sg/~saikit/projects/sceneNN/) | Reconstructions | |
| Coming soon | [2D-3D-S](http://buildingparser.stanford.edu/dataset.html) | Reconstructions | |

## Changelog

Refer to [CHANGELOG.md](CHANGELOG.md) for a record of notable changes.
