---
feature_image: ../assets/images/banner/banner_back.jpg
carousels:
  - images: 
    - image: ../assets/images/gui1.png
    - image: ../assets/images/gui2.png
    - image: ../assets/images/gui3.png
    - image: ../assets/images/gui4.png
---

<div class="presentation-frame centered">
    <div class="index-page-logo">
        <img id="main-logo" src="../assets/logos/logo_1000_adjusted.jpg" alt="BiaPy logo">
    </div>
    <div class="index-page-message">
        <h1>BiaPy</h1>
        <h3>Accessible deep learning on bioimages</h3>
        <a href="https://github.com/BiaPyX/BiaPy/releases/latest" target="_blank" rel="noopener noreferrer">Latest release notes</a>
        <p dir="auto">🔥<strong>NEWS</strong>🔥: BiaPy's paper is finally out in <a href="https://www.nature.com/articles/s41592-025-02699-y"  target="_blank" rel="noopener noreferrer"><strong>Nature Methods</strong></a>! <br>
        [Preprint in <a href="https://www.biorxiv.org/content/10.1101/2024.02.03.576026v3"  target="_blank" rel="noopener noreferrer"><strong>bioRxiv</strong></a>]</p>
    </div>
</div>

<div class="main-frame">
<div class="installation-frame centered central_width">

<!-- <h4>Installation</h4>

<p>There are several options available for executing BiaPy. Choose the method that aligns best with your proficiency, proceed by following the subsequent steps:</p> -->


{% tabs installation %}

{% tab installation GUI %}
<div style="height: 50%">
    <div style="width: 40%; float:left; text-align: center;">
        <a id="download-bn" class="button" style="margin-top: 2rem;" href="https://drive.google.com/uc?export=download&id=1iV0wzdFhpCpBCBgsameGyT3iFyQ6av5o"  target="_blank" rel="noopener noreferrer">
            <svg id="download-bn-icon" role="img" width="32" height="32" class="icon" xmlns="http://www.w3.org/2000/svg"><path d="" fill="#000"></path></svg>
            &nbsp;&nbsp;Download
        </a>
        <div class="more-downloads">
            <span class="text-subtle">Get Additional Installers</span>
            <span class="icon">
                <a id="download-bn2" href="" target="_blank" rel="noopener noreferrer">
                <svg id="download-bn-icon2" role="img" viewBox="0 0 32 32" width="24" height="24" class="icon" xmlns="http://www.w3.org/2000/svg"><path d="" fill="#000"></path></svg>
                </a>
            </span>&nbsp;&nbsp;|&nbsp;&nbsp;
            <span class="icon">
                <a id="download-bn3" href="" target="_blank" rel="noopener noreferrer">
                <svg id="download-bn-icon3" role="img" viewBox="0 0 32 32" width="24" height="24" class="icon" xmlns="http://www.w3.org/2000/svg"><path d="" fill="#000"></path></svg>
                </a>
            </span>
        </div>
        <p style="margin-top: 2rem;">
        Please install <a href="https://www.docker.com/" target="_blank" rel="noopener noreferrer">Docker</a> to use the GUI following <a id="gui_docker_inst_bn" href="" target="_blank" rel="noopener noreferrer">these instructions</a>. 
        <br>
        Find instructions on how to use the GUI <a href="https://www.youtube.com/watch?v=Gnm-VsZQ6Cc&t=41m51s" target="_blank" rel="noopener noreferrer">in this video</a>.
        </p>
        <p>
        You can also <a href="/GUI_versions/" target="_blank" rel="noopener noreferrer">install previous versions of BiaPy's graphical user interface</a>. 
        </p>
    </div>
    <div style="width: 60%; float:left">
        {% include carousel.html height="50" unit="%" duration="7" number="1" %}
    </div>
</div> 
{% endtab %}

{% tab installation Colab Notebooks %}

{% include notebook-carousel.html %}

{% endtab %}

{% tab installation Docker %}

<span id="docker-description" >
We have two container prepared to run BiaPy, one for the actual NVIDIA driver versions and another container for old drivers: 

<div class="docker-container-gallery">
    <div class="grid grid-cols-2 gap-4 p-6">
        <div onclick="window.open('https://hub.docker.com/layers/biapyx/biapy/latest-11.8/images/sha256-86cf198ab05a953ba950bb96fb74b18045d2ed7318afb8fa9b212c97c41be904?context=repo');" class="flex h-full flex-col gap-2 rounded border-gray-light-100 bg-gray bg-white p-4 drop-shadow-sm hover:border-gray-light-200 hover:drop-shadow-lg container-card">
            <div>
                <b>latest-11.8</b><br>
                <i class="fa-brands fa-docker card-icon biapy-colour"></i>
                <table>
                    <tr>
                        <td>Pytorch</td> <td>2.4.0</td>
                    </tr>
                    <tr>
                        <td>CUDA</td> <td>11.8</td>
                    </tr>
                    <tr>
                        <td>Ubuntu</td> <td>22.04</td>
                    </tr>
                </table>
            </div>
        </div>
        <div onclick="window.open('https://hub.docker.com/layers/biapyx/biapy/latest-10.2/images/sha256-c437972cfe30909879085ffd1769666d11875f0ff239df3100fa04ea056d09ab?context=repo');" class="flex h-full flex-col gap-2 rounded border-gray-light-100 bg-gray bg-white p-4 drop-shadow-sm hover:border-gray-light-200 hover:drop-shadow-lg container-card">
            <div>
                <b>latest-10.2</b><br>
                <i class="fa-brands fa-docker card-icon biapy-colour"></i>
                <table>
                    <tr>
                        <td>Pytorch</td> <td>1.12.1</td>
                    </tr>
                    <tr>
                        <td>CUDA</td> <td>10.2</td>
                    </tr>
                    <tr>
                        <td>Ubuntu</td> <td>20.04</td>
                    </tr>
                </table>
            </div>
        </div>
    </div>
</div>


You need to check the CUDA version that you NVIDIA driver can handle. You can do that with ``nvidia-smi`` command in Linux/macOS or by running ``NVIDIA Control Panel`` in Windows. The driver information will tell you the maximum CUDA version it can handle. Select one of the above containers depending on your GPU driver. For instance, if the CUDA version it can handle is ``12.0`` you can use ``biapyx/biapy:latest-11.8`` container. 

Docker Engine is available for Windows, macOS, and Linux, through Docker Desktop. For instructions on how to install Docker Desktop, see:

* <a href="/docker_inst/#win_install">Docker Desktop for Windows</a>
* <a href="/docker_inst/#mac_install">Docker Desktop for Mac (macOS)</a>
* <a href="/docker_inst/#linux_install">Docker Desktop for Linux</a>

<span>

{% endtab %}


{% tab installation Command line %}

You have three different options to install BiaPy. Choose one or another depending on your preferences:

{% tabs command_line_installation %}

{% tab command_line_installation Option 1: Conda + pip %}

To use BiaPy via the command line, you will need to set up a ``conda`` environment. To do this, you will first need to install <a href="https://docs.conda.io/projects/conda/en/stable/" target="_blank" rel="noopener noreferrer">Conda</a>. Then you need to create a ``conda`` environment <a href="/add_ins/#open_terminal">through a terminal</a>:

```bash
conda create -n BiaPy_env python=3.10
conda activate BiaPy_env
```

Then you will need to install <a href="https://pypi.org/project/biapy/" target="_blank" rel="noopener noreferrer">BiaPy package</a> and <a href="https://pytorch.org/get-started/locally/" target="_blank" rel="noopener noreferrer">Pytorch</a>: 

```bash
pip install biapy

# To install with GPU support: Pytorch 2.4.0 + CUDA 11.8
pip install torch==2.4.0 torchvision==0.19.0 torchaudio==2.4.0 --index-url https://download.pytorch.org/whl/cu118 

# Only CPU support: Pytorch 2.4.0 
pip install torch==2.4.0 torchvision==0.19.0 torchaudio==2.4.0 --index-url https://download.pytorch.org/whl/cpu

# Finally install some packages that rely on the Pytorch installation
pip install timm pytorch-msssim torchmetrics[image]==1.4.*
```

The PyPI package does not install <a href="https://pytorch.org/get-started/locally/" target="_blank" rel="noopener noreferrer">Pytorch</a> because there is no option to build that package specifying exactly the CUDA version you want to use. There are a few solutions to set up ``pyproject.toml`` with poetry and specify the CUDA version, as discussed <a href="https://github.com/python-poetry/poetry/issues/6409" target="_blank" rel="noopener noreferrer">here</a>, but then PyPI package can not be built (as stated <a href="https://peps.python.org/pep-0440/#direct-references" target="_blank" rel="noopener noreferrer">here</a>).

<!-- command_line_installation option 1 -->
{% endtab %}

{% tab command_line_installation Option 2: Mamba %}

Before you begin, ensure you have <a href="https://github.com/mamba-org/mamba" target="_blank" rel="noopener noreferrer">Mamba</a> installed. <a href="https://github.com/mamba-org/mamba" target="_blank" rel="noopener noreferrer">Mamba</a> is a faster alternative to <a href="https://docs.conda.io/projects/conda/en/stable/" target="_blank" rel="noopener noreferrer">Conda</a> and can be used to manage your ``conda`` environments. Install ``mamba`` in the base ``conda`` environment, allowing you to use it across all your environments.


If you don't have ``conda`` installed you can download <a href="https://github.com/conda-forge/miniforge#mambaforge" target="_blank" rel="noopener noreferrer">the miniforge installer</a> specific to your OS and run it. Otherwise, if you have ``conda`` already installed just type:

```bash
conda install mamba -n base -c conda-forge
```

Afterwards, create a new <a href="https://docs.conda.io/projects/conda/en/stable/" target="_blank" rel="noopener noreferrer">Conda</a> environment with Python 3.10: 

```bash
mamba create -n BiaPy_env python=3.10
mamba activate BiaPy_env
```

Now you need to install <a href="https://pytorch.org/get-started/locally/" target="_blank" rel="noopener noreferrer">Pytorch</a> and related packages. Double check <a href="https://pytorch.org/get-started/locally/" target="_blank" rel="noopener noreferrer">Pytorch's official page</a> for its specific installation. For example, to install the lastest version of <a href="https://pytorch.org/get-started/locally/" target="_blank" rel="noopener noreferrer">Pytorch</a> with ``conda`` installation in Windows OS under CUDA 12.1: 

```bash
mamba install pytorch torchvision torchaudio pytorch-cuda=12.1 -c pytorch -c nvidia
```

Alternatively, for macOS it would be like this:

```bash
mamba install pytorch::pytorch torchvision torchaudio -c pytorch
```

Then, add extra pytorch related packages: 

```bash
mamba install timm torchmetrics
```

Install BiaPy Dependencies: 

```bash    
mamba install pytz asciitree tzdata typer tqdm torchinfo tifffile threadpoolctl
mamba install six Shapely scipy ruamel.yaml.clib pyparsing protobuf numcodecs lazy_loader kiwisolver
mamba install joblib h5py fonttools fastremap fasteners cycler contourpy zarr=2.16.1 scikit-learn=1.4.0
mamba install scikit-image ruamel.yaml python-dateutil pydot=1.4.2 pandas matplotlib xarray imgaug yaml
mamba install bioimageio.spec bioimageio.core=0.7.0
```

Install packages not available on conda-forge, so install it via pip: 

```bash 
pip install fill-voids pytorch_msssim opencv-python opencv-python-headless imagecodecs==2024.1.1 numpy==1.25.2 pooch tensorboardX==2.6.2.2 yacs==0.1.8 edt==2.3.2
```

Install BiaPy: 

```bash
pip install --no-deps biapy
```

<!-- command_line_installation option 2 -->
{% endtab %}

{% tab command_line_installation Option 3: Developer %}

Set up a ``conda`` environment first by installing <a href="https://docs.conda.io/projects/conda/en/stable/" target="_blank" rel="noopener noreferrer">Conda</a>. Then you need to create a ``conda`` environment <a href="/add_ins/#open_terminal">through a terminal</a>:

```bash
conda create -n BiaPy_env python=3.10
conda activate BiaPy_env
```

To clone the repository you will need to install <a href="https://git-scm.com/" target="_blank" rel="noopener noreferrer">git</a>, a free and open source distributed version control system. Git will allow you to easily download the code with a single command. You can download and install it <a href="https://git-scm.com/downloads" target="_blank" rel="noopener noreferrer">here</a>. For detailed installation instructions based on your operating system, please see the following links: <a href="https://git-scm.com/download/win" target="_blank" rel="noopener noreferrer">Windows</a>, <a href="https://git-scm.com/download/mac" target="_blank" rel="noopener noreferrer">macOS</a> and <a href="https://git-scm.com/download/linux" target="_blank" rel="noopener noreferrer">Linux</a>. 

Once you have installed Anaconda and git, you will need to <a href="/add_ins/#open_terminal">open a terminal</a> to complete the following steps. Then, you are prepared to download <a href="https://github.com/BiaPyX/BiaPy" target="_blank" rel="noopener noreferrer">BiaPy</a> repository by running this command in the terminal:

```bash
git clone https://github.com/BiaPyX/BiaPy.git
```

This will create a folder called ``BiaPy`` that contains all the files of the <a href="https://github.com/BiaPyX/BiaPy" target="_blank" rel="noopener noreferrer">library's official repository</a>. Then you will need to install BiaPy dependencies and for that you need to check the CUDA version that your NVIDIA driver can handle. You can do that with ``nvidia-smi`` command in Linux/macOS or by running ``NVIDIA Control Panel`` in Windows. The driver information will tell you the maximum CUDA version it can handle. We here provide two stable installations, one based in CUDA ``11.8`` and another one with an older version of Pytorch and with CUDA ``10.2`` (BiaPy will work anyway). Once you have checked it, proceed with the installation depending on the CUDA version: 

{% tabs command_line_CUDA_installation %}

{% tab command_line_CUDA_installation CUDA 11.8 %}
```bash
cd BiaPy
pip install --editable .

# Install Pytorch and GPU dependencies
pip install torch==2.4.0 torchvision==0.19.0 torchaudio==2.4.0 --index-url https://download.pytorch.org/whl/cu118 
pip install timm pytorch-msssim torchmetrics[image]==1.4.*
```
{% endtab %}

{% tab command_line_CUDA_installation CUDA 10.2 %}
```bash
cd BiaPy
pip install --editable .

# Install Pytorch and GPU dependencies
pip install pytorch==1.12.1 torchvision==0.13.1 torchaudio==0.12.1 cudatoolkit=10.2 -c pytorch
pip install timm pytorch-msssim torchmetrics[image]==1.4.*
```
{% endtab %}
<!-- command_line_CUDA_installation -->
{% endtabs %} 

<!-- command_line_installation option 3 -->
{% endtab %}

<!-- command_line_installation -->
{% endtabs %}

Verify installation: 

```bash
python -c 'import torch; print(torch.__version__)'
>>> 2.4.0
python -c 'import torch; print(torch.cuda.is_available())'
>>> True
```

<!-- installation Command line  -->
{% endtab %}

<!-- end all tabs -->
{% endtabs %}

</div>
<div id="install-frame-after" class="centered central_width">
</div>
</div>


<div id="four-icons" class="three-icon-frame last_item">
    <ul class="feature-icons">
        <li>
            <a href="https://biapy.readthedocs.io/en/latest/" target="_blank" rel="noopener noreferrer" tabindex="-1" aria-label="follow this link to learn more about biapy" class="icons-color blue1-color">
                    <img src="../assets/images/icons/file-lines-regular.svg" class="docs-icon" alt="docs icon">
            </a>
            <h4><a href="https://biapy.readthedocs.io/en/latest/" target="_blank" rel="noopener noreferrer" class="four-icons-title" aria-label="follow this link to learn more about biapy">Docs</a>
            </h4>
            <p class="four-icons-text">Find BiaPy step-by-step guides, video tutorials and more on <a href="https://biapy.readthedocs.io/en/latest/" target="_blank" rel="noopener noreferrer">ReadTheDocs</a></p>
        </li>
        <li>
            <a href="https://forum.image.sc/tag/biapy" target="_blank" rel="noopener noreferrer" tabindex="-1" aria-label="follow this link to access discussions on the image.sc forum" class="icons-color blue2-color">
                    <img src="../assets/images/icons/comments-regular.svg" class="comment-icon" alt="commnets icon">
            </a>
            <h4><a href="https://forum.image.sc/tag/biapy" target="_blank" rel="noopener noreferrer" class="four-icons-title" aria-label="follow this link to access discussions on the image.sc forum">Discuss</a>
            </h4>
            <p class="four-icons-text">Join other BiaPy users and search discussions on <a href="https://forum.image.sc/tag/biapy" target="_blank" rel="noopener noreferrer">image.sc</a></p>
        </li>
        <li>
            <a href="https://github.com/BiaPyX/BiaPy" target="_blank" rel="noopener noreferrer" tabindex="-1" aria-label="follow this link to the biapy github code base" class="icons-color blue3-color">
                    <img src="../assets/images/icons/code-solid.svg" class="code-icon" alt="code icon">
            </a>
            <h4><a href="https://github.com/BiaPyX/BiaPy" target="_blank" rel="noopener noreferrer" class="four-icons-title" aria-label="follow this link to the biapy github code base">Develop</a>
            </h4>
            <p class="four-icons-text">Check out BiaPy's source code on <a href="https://github.com/BiaPyX/BiaPy" target="_blank" rel="noopener noreferrer">GitHub</a></p>
        </li>
        <li>
            <a href="https://biapy.readthedocs.io/en/latest/get_started/faq.html" target="_blank" rel="noopener noreferrer" tabindex="-1" aria-label="follow this link to the biapy FAQ & Troubleshooting section" class="icons-color blue4-color">
                    <img src="../assets/images/icons/troubleshooting.svg" class="code-icon" alt="code icon">
            </a>
            <h4><a href="https://biapy.readthedocs.io/en/latest/get_started/faq.html" target="_blank" rel="noopener noreferrer" class="four-icons-title" aria-label="follow this link to the biapy FAQ & Troubleshooting section">Troubleshooting</a>
            </h4>
            <p class="four-icons-text">Check out usage tips and documented errors in our <a href="https://biapy.readthedocs.io/en/latest/get_started/faq.html" target="_blank" rel="noopener noreferrer">FAQ & Troubleshooting</a> section</p>
        </li>
    </ul>
</div>

<script>
var OSName = "Unknown";
if (window.navigator.userAgent.indexOf("Windows") != -1) {
    OSName="windows";
} else if (window.navigator.userAgent.indexOf("Mac") != -1) {
    OSName="mac";
} else if (window.navigator.userAgent.indexOf("X11") != -1) {
    OSName="linux";
} else if (window.navigator.userAgent.indexOf("Linux") != -1) {
    OSName="linux";
} else {
    OSName="linux";
}
const OSs = ["linux", "windows", "mac"];
const win_path = "M14.687 16.75h16.309v14.246l-16.12-2.251zM1.004 16.75h12.184v11.81l-12.184-1.69zM14.687 3.44l16.309-2.436v14.246h-16.309zM1.004 5.314l12.184-1.686v11.81h-12.184z"
const linux_path = "M 27.2659 26.4888 C 26.3715 26.1225 25.9889 25.6364 26.0259 24.9111 C 26.064 24.0645 25.5837 23.4444 25.3556 23.1994 C 25.4934 22.673 25.8961 20.852 25.356 19.2703 C 24.7756 17.5773 23.0036 14.9916 21.1752 12.4499 C 20.4267 11.4061 20.3913 10.2715 20.3504 8.9577 C 20.3112 7.7046 20.267 6.2842 19.5682 4.7052 C 18.8084 2.9859 17.2838 2 15.3851 2 C 14.2556 2 13.0962 2.353 12.204 2.9684 C 10.377 4.2293 10.6185 6.9784 10.7783 8.7975 C 10.8002 9.0466 10.8208 9.2819 10.8328 9.4828 C 10.9392 11.2644 10.8424 12.2034 10.7158 12.4888 C 10.6339 12.6753 10.2307 13.2061 9.804 13.7681 C 9.3627 14.3493 8.8624 15.0081 8.4523 15.622 C 7.963 16.3607 7.568 17.4898 7.186 18.5817 C 6.9065 19.3807 6.6425 20.1354 6.3855 20.5864 A 2.7296 2.7296 90 0 0 6.1208 22.6369 C 5.9364 22.765 5.67 23.0172 5.4451 23.4926 C 5.1733 24.0726 4.6218 24.3843 3.475 24.6048 C 2.948 24.7126 2.5846 24.9342 2.3946 25.2634 C 2.1181 25.7425 2.2687 26.3445 2.4061 26.7559 C 2.6091 27.3607 2.4826 27.7435 2.2526 28.4385 C 2.1996 28.5989 2.1395 28.7805 2.0786 28.9808 C 1.9827 29.2969 2.0173 29.5843 2.1812 29.835 C 2.6143 30.4971 3.8781 30.7306 5.1791 30.8842 C 5.9559 30.9764 6.8061 31.2871 7.6284 31.5877 C 8.4341 31.8821 9.2672 32.1866 10.0245 32.279 C 10.1396 32.2935 10.2536 32.3008 10.3635 32.3008 C 11.5069 32.3008 12.0235 31.5421 12.1873 31.2304 C 12.598 31.1466 14.0145 30.8782 15.4744 30.8422 C 16.932 30.8006 18.3423 31.0884 18.7418 31.1779 C 18.8674 31.4183 19.1985 31.9674 19.7263 32.2503 C 20.0164 32.4089 20.4201 32.4998 20.8336 32.4998 H 20.8337 C 21.2753 32.4998 22.1154 32.3954 22.7803 31.6959 C 23.4435 30.9931 25.1005 30.0959 26.3105 29.4408 A 71.787 71.787 90 0 0 27.0546 29.0343 C 27.7343 28.6575 28.1052 28.1191 28.0721 27.5572 C 28.0445 27.0905 27.7356 26.6811 27.2659 26.4888 Z M 12.2189 26.3535 C 12.1343 25.7575 11.3676 25.1664 10.4797 24.482 C 9.7537 23.9223 8.9308 23.288 8.7041 22.7508 C 8.2356 21.6426 8.6049 19.694 9.2488 18.6906 C 9.567 18.1882 9.8269 17.4263 10.0783 16.6895 C 10.3497 15.8939 10.6304 15.0713 10.9443 14.7112 C 11.4414 14.149 11.9008 13.0551 11.9822 12.193 C 12.4477 12.6374 13.1698 13.2013 13.8369 13.2013 C 13.9396 13.2013 14.0393 13.1879 14.1346 13.161 C 14.591 13.0292 15.2623 12.6413 15.9115 12.2663 C 16.4712 11.9429 17.1614 11.5441 17.4211 11.5078 C 17.8664 12.1472 20.4539 17.8733 20.7183 19.7122 C 20.9275 21.1672 20.7065 22.37 20.5954 22.8411 A 2.3017 2.3017 90 0 0 20.2874 22.819 C 19.5667 22.819 19.3759 23.2124 19.3262 23.4473 C 19.1984 24.0576 19.1849 26.0091 19.1835 26.4476 C 18.9229 26.7787 17.605 28.3379 15.7129 28.6182 C 14.9422 28.7302 14.2225 28.787 13.5739 28.787 C 13.0195 28.787 12.6657 28.7442 12.5188 28.7219 L 11.568 27.634 C 11.9429 27.4489 12.3177 27.0583 12.2189 26.3535 Z M 13.4254 8.4149 C 13.3957 8.4277 13.3665 8.4414 13.3378 8.456 A 1.7713 1.7713 90 0 0 13.3179 8.2608 C 13.2141 7.6633 12.8179 7.2296 12.376 7.2296 C 12.3433 7.2296 12.3104 7.2321 12.2743 7.2376 C 12.0114 7.2814 11.8052 7.4789 11.6922 7.7589 C 11.7913 7.1445 12.1394 6.6896 12.5524 6.6896 C 13.0374 6.6896 13.4471 7.3432 13.4471 8.1168 C 13.4471 8.2143 13.44 8.3113 13.4254 8.4149 Z M 17.194 8.8756 C 17.2384 8.7342 17.2624 8.5812 17.2624 8.4224 C 17.2624 7.721 16.8174 7.1715 16.2493 7.1715 C 15.6941 7.1715 15.2424 7.7326 15.2424 8.4224 C 15.2424 8.4694 15.2447 8.5165 15.2491 8.5635 L 15.163 8.5306 A 1.9125 1.9125 90 0 1 15.0668 7.9291 C 15.0668 7.0904 15.6028 6.408 16.2618 6.408 C 16.9207 6.408 17.4568 7.0904 17.4568 7.9291 C 17.4568 8.278 17.3605 8.611 17.194 8.8756 Z M 16.7081 10.508 C 16.6986 10.5504 16.6784 10.5692 16.455 10.6854 C 16.3422 10.7441 16.2018 10.8172 16.0261 10.9242 L 15.9087 10.9953 C 15.4369 11.2813 14.3322 11.9512 14.0323 11.9905 C 13.8286 12.0179 13.7026 11.9389 13.4193 11.7464 A 8.8441 8.8441 90 0 0 13.2149 11.6102 C 12.7042 11.2751 12.3757 10.906 12.3386 10.7617 C 12.5051 10.633 12.9178 10.3109 13.1291 10.1202 C 13.558 9.7214 13.9896 9.4534 14.2032 9.4534 C 14.2145 9.4534 14.2247 9.4542 14.2353 9.4562 C 14.4863 9.5005 15.1054 9.7476 15.5576 9.928 C 15.7666 10.0114 15.9471 10.0834 16.0741 10.129 C 16.4742 10.2664 16.6828 10.4422 16.7081 10.508 Z M 20.3028 29.145 C 20.5285 28.1269 20.7885 26.7419 20.7464 25.9254 C 20.7367 25.7399 20.7203 25.538 20.7044 25.3428 C 20.6747 24.9778 20.6306 24.4353 20.6761 24.2744 C 20.6851 24.2702 20.6951 24.2666 20.7062 24.2635 C 20.7081 24.7303 20.8095 25.6614 21.5541 25.9861 C 21.776 26.0829 22.0296 26.1319 22.3078 26.1319 C 23.0537 26.1319 23.8813 25.766 24.2203 25.427 C 24.4199 25.2274 24.5878 24.9832 24.7054 24.7898 C 24.7311 24.8651 24.7469 24.9635 24.7386 25.0903 C 24.6943 25.7788 25.0289 26.6922 25.6657 27.0288 L 25.7584 27.0775 C 25.9852 27.1965 26.5876 27.5128 26.5973 27.6628 C 26.5972 27.6629 26.5922 27.6805 26.5586 27.7117 C 26.4077 27.8496 25.8766 28.1208 25.363 28.3831 C 24.4519 28.8483 23.4192 29.3756 22.9554 29.8634 C 22.3024 30.5506 21.5638 31.0122 21.1178 31.0122 A 0.483 0.483 90 0 1 20.9717 30.9916 C 20.4873 30.8406 20.0886 30.1417 20.3028 29.145 Z M 3.7917 26.5477 C 3.7423 26.3165 3.7033 26.134 3.7452 25.9572 C 3.7756 25.8262 4.4223 25.6858 4.6985 25.6259 C 5.0868 25.5416 5.4884 25.4545 5.751 25.2951 C 6.1061 25.08 6.2984 24.6833 6.468 24.3333 C 6.5908 24.0802 6.7176 23.8185 6.8685 23.7326 C 6.877 23.7276 6.89 23.7218 6.9148 23.7218 C 7.1975 23.7218 7.7907 24.3161 8.1325 24.848 C 8.2192 24.9821 8.3798 25.2508 8.5656 25.5619 C 9.1213 26.4917 9.8822 27.7652 10.2796 28.192 C 10.6377 28.5757 11.2174 29.3134 11.0748 29.9461 C 10.9704 30.437 10.4146 30.8362 10.2835 30.9245 C 10.2359 30.9353 10.177 30.9408 10.1077 30.9408 C 9.3471 30.9408 7.8415 30.308 7.0326 29.968 L 6.9129 29.9177 C 6.4612 29.7283 5.7238 29.609 5.0107 29.4936 C 4.4433 29.4017 3.6663 29.276 3.5375 29.1624 C 3.4331 29.0453 3.5542 28.6646 3.661 28.3287 C 3.7379 28.0873 3.8173 27.8377 3.8608 27.5764 C 3.9225 27.1596 3.8499 26.8203 3.7917 26.5477 Z"
const mac_path = "M 22.44 16.92 C 22.416 15.6876 22.7364 14.473 23.3654 13.413 C 23.9944 12.353 24.9068 11.4895 26 10.92 C 25.3116 9.9629 24.4126 9.1766 23.3724 8.6218 C 22.332 8.067 21.1784 7.7585 20 7.72 C 17.46 7.52 14.7 9.2 13.68 9.2 C 12.66 9.2 10.14 7.8 8.22 7.8 C 4.22 7.8 -0 10.98 -0 17.32 C 0.0193 19.2962 0.3639 21.2558 1.02 23.12 C 1.9 25.68 5.2 32.1 8.64 32 C 10.44 32 11.72 30.72 14.06 30.72 C 16.4 30.72 17.5 32 19.52 32 C 22.98 32 25.98 26.1 26.84 23.48 C 25.5378 22.9474 24.4238 22.039 23.6402 20.8706 C 22.8564 19.7022 22.4386 18.3268 22.44 16.92 Z M 18.44 5.18 C 19.0614 4.4793 19.53 3.6568 19.8158 2.7649 C 20.1016 1.873 20.1984 0.9314 20.1 0 C 18.2326 0.2048 16.5078 1.0957 15.26 2.5 C 14.6148 3.1798 14.1166 3.9853 13.7966 4.8662 C 13.4766 5.7472 13.3416 6.6846 13.4 7.62 C 14.3684 7.6472 15.3292 7.4395 16.1998 7.0146 C 17.0706 6.5896 17.8254 5.9602 18.4 5.18 H 18.44 Z"

// Change the main download button icon and link
const elem = document.getElementById("download-bn-icon");
const elem2 = document.getElementById("download-bn");
elem.setAttribute('alt', OSName);
if (OSName === "linux") {
    elem.childNodes[0].setAttribute('d', linux_path);
    elem2.setAttribute('href', "https://drive.google.com/uc?export=download&id=13jllkLTR6S3yVZLRdMwhWUu7lq3HyJsD")
} else if (OSName === "windows") {
    elem.childNodes[0].setAttribute('d', win_path);
    elem2.setAttribute('href', "https://drive.google.com/uc?export=download&id=1iV0wzdFhpCpBCBgsameGyT3iFyQ6av5o");
} else {
    elem.childNodes[0].setAttribute('d', mac_path);
    elem2.setAttribute('href', "https://drive.google.com/uc?export=download&id=1fIpj9A8SWIN1fABEUAS--DNhOHzqSL7f");
} 

// Remove the value 
const index = OSs.indexOf(OSName);
if (index > -1) { 
  OSs.splice(index, 1);
}
// Fill additional downloads 
for (let i = 0; i < OSs.length; i++) {
    const elem = document.getElementById("download-bn-icon"+(i+2));
    const elem2 = document.getElementById("download-bn"+(i+2));
    if (OSs[i] === "linux") {
        elem.childNodes[0].setAttribute('d', linux_path);
        elem2.setAttribute('href', "https://drive.google.com/uc?export=download&id=13jllkLTR6S3yVZLRdMwhWUu7lq3HyJsD");
    } else if (OSs[i] === "windows") {
        elem.childNodes[0].setAttribute('d', win_path);
        elem2.setAttribute('href', "https://drive.google.com/uc?export=download&id=1iV0wzdFhpCpBCBgsameGyT3iFyQ6av5o");
    } else {
        elem.childNodes[0].setAttribute('d', mac_path);
        elem2.setAttribute('href', "https://drive.google.com/uc?export=download&id=1fIpj9A8SWIN1fABEUAS--DNhOHzqSL7f");
    } 
}

//
const elem3 = document.getElementById("gui_docker_inst_bn")
if (OSName === "linux") {
    elem3.setAttribute('href', "/docker_inst/#linux_install");
} else if (OSName === "windows") {
    elem3.setAttribute('href', "/docker_inst/#win_install");
} else {
    elem3.setAttribute('href', "/docker_inst/#mac_install");
} 
</script>