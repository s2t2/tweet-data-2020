
# Contributor's Guide

Here are some steps used in the maintenence of this repository.

## Git LFS

The data is large, so we need to use [Git Large File Storage](https://git-lfs.github.com/) BEFORE EVER COMMITTING ANY OF THE LARGE FILES:

```sh
git lfs install
```

```sh
git lfs track "*.csv"
git lfs track "*.zip"
```

```sh
git add .gitattributes
```

Then commit the file.

## Queries

Queries used to export this data found [here](https://github.com/s2t2/tweet-analysis-2020/issues/73#issuecomment-1273587960).


