# Utility Script for Copying Files

## Functionality 

The script is designed to iterate over all images found through the ```input_file_pattern```, giving three input options for each image. Note that the images are sorted prior to being displayed, meaning that they should be displayed in the order in which they were taken.  

The first user input defines ```Tag``` which should be the tag associated with the image. The second is ```Rank``` which defines the rank of the individual and the third is ```save``` which defines whether the image should be copied and renamed to the ```output_dir```. The input variables remain until being changed meaning that they don't have to be changed if they stay the same ("if you have multiple images from the same Tag, Rank that should be saved"). Please note that the folder name of the directory containing the images is used to define the date in the new destination filename.  

File name convention is:
```RBVVV_WWWW_RankX_YYYY_ZZZ.FFF```
Where ```VVV``` is the ***Tag number***, ```WWWW``` is the ***folder name containing the image*** (ideally the date collected), ```X``` is the defined ***Rank***, ```YYYY``` is the ***image name as given by the camera or before renaming***, ```ZZZ``` is a ***continuous image index*** given to each image when renaming and copying and ```FFF``` is the same ***file extension*** as the original image file.

## Installation

### 1. Using Visual Studio Code <font style="font-weight: 100">[Recommended]</font>

1. Download this repository by clicking on the green ```Code``` button and selecting "Download ZIP" at the top left of the repository page. Alternatively you can run the following command in a terminal:  
<p style="text-align: center;"><code>git clone https://github.com/fritzfrancisco/FileRenamingHelper.git</code></p>
  
2. [Download](https://code.visualstudio.com/download) and [install](https://code.visualstudio.com/docs/getstarted/introvideos) Visual Studio Code following the given instructions on their website.

3. [Install Miniconda](https://docs.anaconda.com/miniconda/miniconda-install/) (Recommemded) or Anaconda to have access to ```conda``` utilities. Further information is also available [here](http://fritzfrancisco.thekaolab.com/assets/content/pdf/python_setup_guide_22092020.pdf).

4. Create ```conda``` environment following the instructions given [here](https://code.visualstudio.com/docs/python/environments), specifically under "Create a conda environment in the terminal". We will be using an environment named ```filecopy``` in the following, but feel free to name it anything you wish and can remember. This is the command to do so:

<p style="text-align: center;"><code>conda create -n filecopy -c conda-forge python=3.11 pandas numpy pip matplotlib glob2 opencv</code></p>

5. Open Visual Studio Code. If the bottom left says "Restricted" click on it and set the mode to "Trust".

6. Install ```Python``` support through the Extension Menu on the right. Open the menu and type ```python``` the first extension given should be the correct one to install, for Python support in VS Code.

7. Install ```Code Runner``` Extension by going to the Extension Menu on the right. Type ```Code Runner``` into the search bar and install it. Once finished installing press ```CTRL + ,``` and type ```code runner``` to locate it. Scroll down and check on ```Code-runner: Run In Terminal```.

8. In Visual Studio Code, select interpreter by pressing ```CTRL + SHIFT + P``` > Python: Select Interpreter > ```ENTER``` and selecting the ```conda``` environment that was just created. It should be named ```filecopy```.

9. Now we can open the [Jupyter Notebook](https://jupyter.org/) ```FileRenamingHelper.ipynb``` > File > Open File... > Navigate to the designated file. If the ```conda``` environment was set correctly the name of it should appear in the bottom or top right when opening the notebook.

10. Run first cell to import all required packages. This is done by either clicking the play symbol in front of it or selecting it and pressing ```Super + ENTER```. Follow any pop-ups to install further requirements for Visual Studio Code.


### 2. Using basic Jupyter Notebook

1. [Install Miniconda](https://docs.anaconda.com/miniconda/miniconda-install/) (Recommemded) or Anaconda to have access to ```conda``` utilities. Further information is also available [here](http://fritzfrancisco.thekaolab.com/assets/content/pdf/python_setup_guide_22092020.pdf).

2. Create ```conda``` environment following the instructions given [here](https://code.visualstudio.com/docs/python/environments), specifically under "Create a conda environment in the terminal". We will be using a environment named ```filecopy``` in the following, but feel free to name it anything you wish and can remember. You can alternatively use the supplied ```environment.yaml``` file and the following command to do so:

3. Activate ```conda``` environment by opening a terminal (Linux, Mac OS) or Anaconda Prompt (Windows) and typing:

<p style="text-align: center;">
<code>conda activate filecopy</code>
</p>

4. Install [Jupyter Lab](https://anaconda.org/conda-forge/jupyterlab) by running:
<p style="text-align: center;"><code>conda install conda-forge::jupyterlab</p></code></p>
    
5. Open [Jupyter Notebook](https://jupyter.org/) by running: 
<p style="text-align: center;"><code>cd /path/to/directory/containing/FileRenamingHelper/notebook</code><br>
<br>
<code>jupyter lab</code></p>


## Usage

1. Open [Jupyter Notebook](https://jupyter.org/) following the instructions in the installation section. Update ```input_file_pattern``` and ```output_dir``` to match your requirements in Cell 2 and run it. Be sure to make sure to account for differences between Unix and Windows and ideally not having blank spaces in filenames! I would recommend using only '/' in all file paths, as the script should account for it. Note, if the ```output_dir``` does not exist yet it will be created by running Cell 2.

2. Run Cells 1-2 to import required libraries and set corresponding path variables.
 
3. Run Cell 3, which should start displaing an image and open an input field. Input the corresponding values and press ```Enter``` to confirm. If you make a mistake the easiest way to undo it is to rename the last mistakable labeled file manually and changing the values for ```Tag``` and ```Rank``` on the next image, as they will be updated and kept this way.

4. Lastly, if you want to stop and continue at a later point in time, you can do so. Just keep track of the continuous image index and change the ```start_file``` variable to the number you want to continue on. This does not work across directories, since when you change the directory the number of images changes and everything should be started from a fresh session!

## Note
Additional notebooks are supplied for image rectification and camera calibration which are not further explained in this README.  

Please contact [Fritz A. Francisco](mailto:fritz.a.francisco@gmail.com?subject=[GitHub]%20Source%20Han%20Sans) with any further information, requests, complaints or suggestions. 
