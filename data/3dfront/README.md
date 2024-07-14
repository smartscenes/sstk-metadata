The 3DFront dataset can be downloaded from https://tianchi.aliyun.com/specials/promotion/alibaba-3d-scene-dataset

Once you have downloaded the 3DFront and 3DFuture datasets, unzip `3D-FRONT.zip` and `3D-FUTURE-model.zip` and place them into the same directory as follows:
```
${3DFRONT_ROOT}
 |-- 3D-FRONT                      # 3D-FRONT.zip        unzipped (each scene is a separate json file)
     |-- <sceneId>.json
 |-- 3D-FUTURE-model               # 3D-FUTURE-model.zip unzipped (each model is a separate directory)
     |-- <modelId>
         |-- image.jpg
         ├── model.mtl         
         ├── normalized_model.obj
         ├── raw_model.obj
         ├── texture.png
```

Copy metadata files in this directory into `${3DFRONT_ROOT}`
```
${3DFRONT_ROOT}
|-- 3dfront.models.metadata.json   # metadata file for 3DFUTURE models
|-- 3dfront.scenes.metadata.json   # metadata file for 3DFRONT scnes
```

To use these assets with the SmartScenes Toolkit (SSTK), 
```
# symlink `${3DFRONT_ROOT}` to `${SSTK}/server/static/data/3dfront`
ln -s ${3DFRONT_ROOT} ${SSTK}/server/static/data/3dfront
```

Once you have hooked up the 3DFRONT and 3DFUTURE assets with the SSTK, you can use the SSTK to render images for 3DFRONT and place the renderings under `${3DFRONT_ROOT}/3D-FRONT-renders`.  The expected directory structure is:
```
${3DFRONT_ROOT}
 |-- 3D-FRONT-renders                      
     |-- <sceneId>.png
```


