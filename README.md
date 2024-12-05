# Pypi Study Using `hatchling` for pure Python Package

## Dependency

```angular2html
pip3 install build twine numpy requests auditwheel
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

## Fix the wrong platform tag issue

As `linux_x86_64` is not supported, we need to make the platform tag more compatible.


```
auditwheel repair dist/pypatchworkpp-1.0.1-cp38-cp38-linux_x86_64.whl
```

But sometimes, the following error happens:

```
auditwheel repair dist/pypatchworkpp-1.0.1-cp38-cp38-linux_x86_64.whl
INFO:auditwheel.main_repair:Repairing pypatchworkpp-1.0.1-cp38-cp38-linux_x86_64.whl
usage: auditwheel [-h] [-V] [-v] command ...
auditwheel: error: cannot repair "dist/pypatchworkpp-1.0.1-cp38-cp38-linux_x86_64.whl" to "manylinux_2_5_x86_64" ABI because of the presence of too-recent versioned symbols. You'll need to compile the wheel on an older toolchain.
```

---

## Results

![](/materials/pypi_result.png)

