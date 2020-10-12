# CSCI-566 Assignment 2

## The objectives of this assignment
* Implement Variational Autoencoders (VAEs)
* Implement Generative Adversarial Networks (GANs)

## Working on the Assignment
**We highly recommend the use of Google Colab, so that you can use free GPUs to speed up training.**

Without it, training will be painfully slow.

To do this, simply click on the "Open in Colab" button at the top of each notebook while viewing the notebook on Github (or locally). Make sure to right click -> open in new tab for it to work on Github.

You can then make a copy of the notebook in Google Colab (`Copy to Drive`) and start working on it!

**Remember to use a GPU**: Click Runtime -> Change runtime type -> Select GPU as the Hardware accelerator.

If you really want to use your own computer, see the following instructions:
________________________________________________________
In this assignment, please use Python `3.6`.
You will need to make sure that your virtualenv setup is of the correct version of python.

Please see below for executing a virtual environment.
```shell
cd csci566-assignment2
pip3 install virtualenv # If you didn't install it

# replace your_virtual_env with the virtual env name you want
virtualenv -p $(which python3) your_virtual_env
source your_virtual_env/bin/activate

# install dependencies
pip3 install -r requirements.txt

# work on the assignment
deactivate # Exit the virtual environment
```
To start working on the assignment, simply run the following command to start an ipython kernel.
```shell
# add your virtual environment to jupyter notebook
source your_virtual_env/bin/activate
python -m ipykernel install --user --name=your_virtual_env

# port is only needed if you want to work on more than one notebooks
jupyter notebook --port=your_port_number

```
and then work on each problem with their corresponding `.ipynb` notebooks.
Check the python environment you are using on the top right corner.
If the name of environment doesn't match, change it to your virtual environment in "Kernel>Change kernel".

## Problems
In each of the notebook file, we indicate `TODO` or `Your Code` for you to fill in with your implementation.

### Problem 1: Variational Autoencoders (45 points)
The IPython Notebook `CSCI566_Assignment2_problem_1_VAE.ipynb` will walk you through implementing VAEs with PyTorch.

### Problem 2: GANs for Image Generation (37 points)
The IPython Notebook `CSCI566_Assignment2_problem_2_GAN.ipynb` will walk you through implementing a GAN with PyTorch.

## How to submit

Run the following command to zip all the necessary files for submitting your assignment. Note that, in addition to your notebook **with all cell outputs** you will need to manually create a submission PDF for each problem set that compiles all generated plots / answers. Detailed instructions are at the end of the notebooks. The command below aggregates all notebooks and solution PDFs.

**If using Colab, remember to download the .ipynb files locally!!!**

```shell
sh collectSubmission.sh
```

This will create a file named `assignment2.zip`, **please rename it with your usc student id (eg. 4916525888.zip)**, and submit this file through the [Google form](https://docs.google.com/forms/d/e/1FAIpQLSdh6Qtqc81a4fJEuGRbF8o9Gxtr5vr7rbBOyluCgYTAsPdmoQ/viewform?usp=pp_url).
Do NOT create your own .zip file, you might accidentally include non-necessary materials for grading.
We will deduct points if you don't follow the above submission guideline.

**VERIFY THAT THE `assignment2.zip` CONTAINS THE IPYNB FILES AND THE PDFS**

**!! SUBMIT YOUR NOTEBOOK INCLUDING ALL CELL OUTPUTS, WE WILL NOT RERUN YOUR NOTEBOOKS !!**

## Questions?
If you have any question or find a bug in this assignment (or even any suggestions), we are more than welcome to assist through Piazza.

Again, NO INDIVIDUAL EMAILS WILL BE RESPONDED.

PLEASE USE **PIAZZA** TO POST QUESTIONS (under folder assignment1).

## FAQ

- Can I reuse the virtualenv from Assignment 1?
You can reuse the vistual environment but maybe you need to install some missing packages using pip3 install -r requirements.txt.
Maybe simpler is to create a new virtualenv, we give instructions above.
- My reconstruction loss for Problem 2.4 is higher than 0.145?
You should achieve a reconstruction loss lower than 0.145 for full credit.

- **General debugging tips**
1. Make sure your implementations matches the specified model layers perfectly.
2. Put print statements at various places inside your implementation code to make sure every module is working as it should. 
(but please remove any additional print statements for submission)
