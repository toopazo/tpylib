# toopazo_tools
A personal python library for common file-processing tasks

Important links
- https://packaging.python.org/tutorials/packaging-projects/
- https://pypi.org/

## How to upload a new version
This is taken from https://widdowquinn.github.io/coding/update-pypi-package/

1. Update local packages for distribution
    ```
    python3 -m pip install --user --upgrade setuptools wheel
    python3 -m pip install --user --upgrade twine 
    ```
2. Open setup.py and change the version, e.g., version='1.0.3'.
It is sometimes neccessary to delete the build/ anddist/ folder
    ```
    rm -r build/*
    rm -r dist/*
    ```
3. Create distribution packages on your local machine, and check
the dist/ directory for the new version files
    ```
    python3 setup.py sdist bdist_wheel
    ```
4. Upload the distribution files to https://pypi.org/ server
    ```
    python3 -m twine upload dist/*
    ```
5. Install the package from https://pypi.org/ server
    ```
    python3 -m pip install -U toopazo-tools
    ```



