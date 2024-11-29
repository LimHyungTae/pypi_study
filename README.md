# Pypi Study Using `hatchling` for pure Python Package

## Dependency

```angular2html
pip3 install build twine numpy
```

`numpy` is to test the dependency in the Pypi package


## How to build

```
python3 -m build
```

```
python3 -m twine upload dist/*
```

Then, you can see the printed command lines as below:

![](/materials/1129_pypi_commandline.png)


## Results

![](/materials/pypi_result.png)

