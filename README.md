
# W2MHS - Wisconsin White Matter Hyperintensities Segmentation Toolbox
#### Wisconsin Alzheimer’s Disease Research Center, UW-Madison
#### 2018

## About
This document only contains installation and using instructions for GUI users.
Please refer to [W2MHS](https://github.com/SichaoYang/W2MHS) for more details about the project, source code and commandline interface.

## Branches
source: Matlab source code for users with Matlab installed.

linux: installer for Linux users.

windows: installer for Windows users.

macos: installer for MacOS users.

## Installation
1. Install [docker](https://docs.docker.com/install/)

2. (Mac) Run ```sudo ln -s `which docker` /bin``` in the terminal.

3. Download and unzip the W2MHS toolbox.

4. Run Matlab with root/administrator permissions:
    - (Windows) Right click Matlab and click "run as administrator".
    - (Linux & MacOS) Run ```matlabroot``` in Matlab console and copy the returned path ```/.../MATLAB...```. Then run ```sudo /.../MATLAB.../bin/matlab``` in the terminal.

5. Navigate Matlab to the root directory of the toolbox.

6. Run ```installW2MHS``` in Matlab console.

7. Run ```W2MHS``` in Matlab console.

## Usage
1. Enter *W2MHS Toolbox Path*, *SPM Toolbox Path*, and *Output Path*, as well as *Output Name*
as the shared prefix of the output folders of all subjects.

2. Add subjects using the "Add T1 and T2 Volumes" button. Remove a subject from the batch by selecting
it and pressing the ”Remove Selected” button.
    
    The add subjects button will allow you to add one subject at a time or select a directory that contains
a batch of T1 and T2 image pairs. To use the directory batch function, the images must follow the naming
convention described in the *BatchSetup.m* script. Each subject must have a unique name or identifier
which is the Subject ID. If you enter one subject at a time make sure to enter this field and make sure
they are all unique. When using the directory batch function make sure that the subjects it imports are
automatically assigned Subject IDs.

3. (Optional) Use *Set Default* on the menu bar to set the default configuration of the GUI. You may
want the GUI to store both the SPM12 and W2MHS toolbox paths. Setting a new default will overwrite
the old configuration. Also, Use *Save* to save sessions to ’.mat’ files and *Load* them later.

4. (Optional) Set the advanced options as explained in *param.m*.

5. Click *Run* to start.
