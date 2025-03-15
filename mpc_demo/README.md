# CrypTen
### Ofer's descryption

https://github.com/facebookresearch/CrypTen     
https://pypi.org/project/crypten/            


## Use the ***crypten*** conda environment

## Setup CrypTen

1) Add tmp folder under mpc_demo/          
		$ mkdir tmp

2)     
### *** FIX THE SKLEARN DEPENDENCY ISSUE! ***
crypten depends on 'sklearn' that is deprecated and now should be 'scikit-learn'.
Install 'scikit-learn' seperatelly and set the following environment variable to avoid an error:
SKLEARN_ALLOW_DEPRECATED_SKLEARN_PACKAGE_INSTALL=True
Set it in the ~/.profile file:
	export SKLEARN_ALLOW_DEPRECATED_SKLEARN_PACKAGE_INSTALL=True

---------------------------------------------------------------------------

3)     
## Set the 'crypten' conda environment:    

## conda-forge
An opensource conda           
https://conda-forge.org       
https://github.com/conda-forge/miniforge           

4)    
After installation, add the following in .bashrc:              
===============================================================
In .bashrc
==========

# For conda I am using the opensourse miniforge
# https://conda-forge.org
# https://github.com/conda-forge/miniforge

# >>> conda initialize >>>
# !! Contents within this block are managed by 'conda init' !!
__conda_setup="$('/home/orivlinux/miniforge3/bin/conda' 'shell.bash' 'hook' 2> /dev/null)"
if [ $? -eq 0 ]; then
    eval "$__conda_setup"
else
    if [ -f "/home/orivlinux/miniforge3/etc/profile.d/conda.sh" ]; then
        . "/home/orivlinux/miniforge3/profile.d/conda.sh"
    else
        export PATH="/home/orivlinux/miniforge3/bin:$PATH"
    fi
fi
unset __conda_setup
# <<< conda initialize <<<

export PATH="/home/orivlinux/bin:$PATH"

===============================================================

5)    

	$ conda create -n crypten python=3.7.0
	$ conda activate crypten
	$ python --version
	Python 3.7.0

Install the following packages:    

	$ conda install matplotlib
	$ conda install pandas
	$ conda install seaborn

----------------------------------------------------
In case you use the regular licensed conda, install the conda packages like so:

	$ conda install conda-forge::matplotlib
	$ conda install anaconda::pandas
	$ conda install anaconda::seaborn
----------------------------------------------------

6)     

pip installations:

The file requirements_ofer.txt is under mpc_demo/    
	$ pip install -r requirements_ofer.txt

or separately:

	$ pip install scikit-learn
	$ pip install chardet
	$ pip install jupyter
	$ pip install notebook
	$ pip install jupyterlab
	$ pip install ipython
	$ pip install ipykernel
	$ pip install ipywidgets


7)    
*** Make sure you added the fix in the .profile file, for the sklearn issue as explained in #2 above     

	$ source ~/.profile
	$ conda activate crypten
	$ pip install crypten
	$ pip install -r requirements.examples.txt

	$ python -m ipykernel install --user --name=crypten
	Installed kernelspec crypten in /home/ofer/.local/share/jupyter/kernels/crypten

	$ jupyter lab
	or
	$ jupyter lab  --no-browser


