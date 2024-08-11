# Utility Script for Copying Files

## Functionality 

The script is designed to iterate over all images found through the ```input_file_pattern```, giving three input options for each image. Note that the images are sorted prior to being displayed, meaning that they should be displayed in the order in which they were taken.  
 The first user input defines ```Tag``` which should be the tag associated with the image. The second is ```Rank``` which defines the rank of the individual and the third is ```save``` which defines whether the image should be copied and renamed to the ```output_dir```. The input variables remain until being changed meaning that they don't have to be changed if they stay the same ("if you have multiple images from the same Tag, Rank that should be saved"). Please note that the folder name of the directory containing the images is used to define the date in the copied filename.

## Installation

### 1. Using Visual Studio Code <font style="font-weight: 100">[Recommended]</font>

1. [Download](https://code.visualstudio.com/download) and [install](https://code.visualstudio.com/docs/getstarted/introvideos) Visual Studio Code following the given instructions on their website.

2. [Install Miniconda](https://docs.anaconda.com/miniconda/miniconda-install/) (Recommemded) or Anaconda to have access to ```conda``` utilities. Further information is also available [here](http://fritzfrancisco.thekaolab.com/assets/content/pdf/python_setup_guide_22092020.pdf).

3. Create ```conda``` environment following the instructions given [here](https://code.visualstudio.com/docs/python/environments), specifically under "Create a conda environment in the terminal". We will be using a environment named ```filecopy``` in the following, but feel free to name it anything you wish and can remember. You can alternatively use the supplied ```environment.yaml``` file and the following command to do so:

<p style="text-align: center;"><code>conda create -f /path/to/environment.yaml</code></p>

4. Open Visual Studio Code. If the bottom left says "Restricted" click on it and set the mode to "Trust".

5. Install ```Code Runner``` Extension by going to File > Preferences > Settings. Typ ```Code Runner``` into the search bar and install it. Scroll down and check on ```Code-runner: Run In Terminal```. Alternatively you can select it through the Extensions menu on the left side of the screen.

6. Select interpreter by pressing ```CTRL + SHIFT + P``` > Python: Select Interpreter > ```ENTER``` and selecting the ```conda``` environment that was just created. It should be named ```filecopy```.

7. Now we can open the [Jupyter Notebook](https://jupyter.org/) ```FileRenamingHelper.ipynb``` > File > Open File... > Navigate to the designated file. If the ```conda``` environment was set correctly the name of it should appear in the bottom right, when opening the notebook.

8. Run first cell to import all required packages. This is done by either clicking the play symbol in front of it or selecting it and pressing ```Super + ENTER```. Follow any pop-ups to install further requirements for Visual Studio Code.


### 2. Using basic Jupyter Notebook

1. [Install Miniconda](https://docs.anaconda.com/miniconda/miniconda-install/) (Recommemded) or Anaconda to have access to ```conda``` utilities. Further information is also available [here](http://fritzfrancisco.thekaolab.com/assets/content/pdf/python_setup_guide_22092020.pdf).

2. Create ```conda``` environment following the instructions given [here](https://code.visualstudio.com/docs/python/environments), specifically under "Create a conda environment in the terminal". We will be using a environment named ```filecopy``` in the following, but feel free to name it anything you wish and can remember. You can alternatively use the supplied ```environment.yaml``` file and the following command to do so:

3. Activate ```conda``` environment and open [Jupyter Notebook](https://jupyter.org/) by opening a terminal (Linux, Mac OS) or Anaconda Prompt (Windows) and typing:

<p style="text-align: center;"><code>cd /path/to/location/of/FileRenamingHelper.ipynb</code><br>
<br>
<code>conda activate nameofyourenvironment</code><br>
<br>
<code>jupyter notebook</code></p>

## Usage

1. Open [Jupyter Notebook](https://jupyter.org/) following the instructions in the installation section. Update ```input_file_pattern``` and ```output_dir``` to match your requirements in Cell 2 and run it. 

2. Run Cell 3, which should display an image and open an input field.
