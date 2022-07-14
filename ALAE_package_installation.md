# ALAE Package Installation

## Preprocessing</br>

#### Please notice below operations only for Windows platform</br>

1. When your computer didn't install the python please download python installer at https://python.org, at this time you should choice the python3.7 - python3.9 to fit the pytorch.
2. Please uptodate yor NVIDIA GPU driver to newest version at: https://www.nvidia.cn/geforce/drivers/
3. Please download CUDA installer at: https://developer.nvidia.com/cuda-11-6-2-download-archive and select your platform to fit the torch version.
4. Please download cuDNN archiver at: https://developer.nvidia.cn/rdp/cudnn-download, beforce this operation you should sigin the nvidia developer account, and agree license agreement. Extract and copy the bin, include, lib into CUDA Development folder.
5. Install the PyTorch for your environment, please check the PyTorch office website for helping your installation. Example you need the GPU version for your torch, at same time you use the pip to organize your objects please run `pip3 install torch torchvision torchaudio --extra-index-url https://download.pytorch.org/whl/cu116`, but you have to conform your CUDA, GPU driver, Python, their version is fit.
6. Predownload package bimpy for dlutils package requirement at:https://github.com/podgorskiy/bimpy, please notece the libs doesn't precompiled, and at github pages to download thats files
    ```Html
        backward-cpp: https://github.com/bombela/backward-cpp/tree/27a89004a86fe2a665f041c198c7fbab7489e278
        gl3w: https://github.com/skaslev/gl3w/tree/7729692af8a2322cddb636b90393a42c130b1c85
        glfw: https://github.com/glfw/glfw/tree/0a49ef0a00baa3ab520ddc452f0e3b1e099c5589
        imgui: https://github.com/ocornut/imgui/tree/58b3e02b95b4c7c5bb9128a28c6d55546501bf93
        pybind11: https://github.com/pybind/pybind11/tree/f1abf5d9159b805674197f6bc443592e631c9130
    ```
    for libs folder, download them as zip files  and extract at here. Please back bimpy root folder, and run:
    ```Bash
            $ python setup.py bdist_wheel
    ```
    when you compiled this package to a whl file, you can find that at 'dist' folder.
    While now you could able to install the whl file for your python environment.

7. Run `pip install -r requirements.txt` at ALAE root folder to install this object need requirement packages.

8. Next step you need to predownload the training modules for ALAE, but the code was too old, you should block 
    ```Python
        from torch.autograd.gradcheck import zero_gradients
    ```
    this code was not supported at PyTorch 11.2, please comment it at [__init__.py]($PYTHONPATH\Lib\site-packages\dlutils\__init__.py), and [__init__.py]($PYTHONPATH\Lib\site-packages\dlutils\pytorch\__init__.py), finally you could run `python training_artifacts/download_all.py` to download the training modules. Next have a rest waiting for downloading.

9. At last step we need install named auto-attack package in this python environment, to instead that commented code. Now type [auto-attack](`$ pip install git+https://github.com/fra31/auto-attack`) in your terminal, make the installation complete. When you can't connect to the github server, please move to auto-attacks offical github page, and download the zip archiver manually. Extract it and open terminal in that folder, `$ python setup.py install` this command will automatic help you install this package.
10. Now open that two files in step 8, add `from autoattack.other_utils import zero_gradients` this line under commented code.
11. Next step, is on the way ...