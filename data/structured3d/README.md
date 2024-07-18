The original Structured3D dataset can be downloaded from https://structured3d-dataset.org/.  

To use the extracted architectures from the Structured3D dataset with the SSTK, please get the architecture files from https://huggingface.co/datasets/3dlg-hcvc/structured3d-arch.

Once you obtain access to the dataset, following [the huggingface instructions](https://huggingface.co/datasets/3dlg-hcvc/structured3d-arch?clone=true) to clone the repo.
```
# Make sure you have git-lfs installed (https://git-lfs.com)
git lfs install

# Make sure your SSH key is properly setup in your user settings.
# https://huggingface.co/settings/keys
git clone git@hf.co:datasets/3dlg-hcvc/structured3d-arch
```

They should be organized as follows
```
${STRUCTURED3D_ARCH_ROOT}
 |-- arch                       # JSON files specifying the architecture
 |-- arch_renders               # Renderings of the architecture
```

Copy metadata files in this directory into `${STRUCTURED3D_ARCH_ROOT}`
```
cp structured3d.* ${STRUCTURED3D_ARCH_ROOT}
```

The metdata files in the directory includes:
```
${STRUCTURED3D_ARCH_ROOT}
|-- structured3d.arch.metadata.json    # metadata file for structured3d architecture
|-- structrued3d.scenes.csv            # list of scenes in the structured3d dataset
|-- structrued3d.rooms.csv             # list of rooms in the structured3d dataset
```

To use these assets with the SmartScenes Toolkit (SSTK), 
```
# symlink `${STRUCTURED3D_ARCH_ROOT}` to `${SSTK}/server/static/data/structured3d`
ln -s ${STRUCTURED3D_ARCH_ROOT} ${SSTK}/server/static/data/3dfront
```
