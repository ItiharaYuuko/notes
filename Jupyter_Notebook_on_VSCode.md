# Operate ".ipynb" files on VSCode
#### Attention: Below operations all tested on windows, other platform didn't test
1. Install "jupyter notebook" and "ipykernel" library on your python environment.
    ```bash
    > pip install jupyter notebook ipykernel
    ```
2. Waiting for pip downloading and installing library files into your machine.
3. Type under commands and codes in your bash or cmd to test upon libraries installation.
    ```bash
    > python
    ```
    ```python
    >>> import jupyter notebook ipykernel
    >>> notebook.__version__
    >>> ipykernel.__version__
    >>> exit()
    ```
    ```bash
    > jupyter notebook
    ```

# Let jupyter notebook and VSCode jypyter notebook extension support the PDF export function

1. Install "pyppeteer" "nbconvert" "PyQtWebEngine" libraries.
    ```bash
    pip install pyppeteer nbconvert PyQtWebEngine
    ```
2. Install [MiKTex](https://miktex.org/download#win) and [pandoc](https://www.pandoc.org/installing.html) manually
3. Add the MikTex and pandoc binary path into your system environment arguments path.
4. Turn your VSCode or jupyter notebook to test "Export PDF" or "Download as PDF(LaTex)" functionality.