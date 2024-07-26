The [Habitat Synthetic Scenes Dataset (HSSD)](https://3dlg-hcvc.github.io/hssd/) dataset can be downloaded from https://huggingface.co/hssd.

The HSSD dataset consists of several different repositories
`hssd/hssd-models` - Original HSSD 3D assets
`hssd/hssd-sstk` - HSSD scenes (scenes in SSTK compatible JSON format)
`hssd/hssd-hab` - Habitat compatible objects and scenes 

To setup HSSD dataset for use with the SSTK, create a directory `${HSSD_ROOT}` and clone the repositories as needed.
The directory structure should be:
```
${HSSD_ROOT}
|-- hssd-models      # For extracted 3D objects.  
                     # git clone git@hf.co:datasets/hssd/hssd-models
|-- hssd-sstk        # For scenes in SSTK compatible JSON format
                     # git clone git@hf.co:datasets/hssd/hssd-sstk
|-- hssd-hab         # For habitat compatible 3D objects and scenes
                     # git clone git@hf.co:datasets/hssd/hssd-hab
```

Copy metadata files in this directory into `${HSSD_ROOT}`
```
${HSSD_ROOT}
|-- fp.models.metadata.json - metadata for hooking up HSSD object assets
|-- fp.scenes.metadata.json - metadata for hooking up HSSD scene assets
```

To use these assets with the SmartScenes Toolkit (SSTK), 
```
# symlink `${HSSD_ROOT}` to `${SSTK}/server/static/data/hssd`
ln -s ${HSSD_ROOT} ${SSTK}/server/static/data/hssd
```

