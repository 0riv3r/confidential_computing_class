# Confidential Computing Class - notebooks

## conda-forge
An opensource conda           
https://conda-forge.org       
https://github.com/conda-forge/miniforge           

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

Install the following packages:     

    $ conda install sympy
    $ conda install scipy
    $ conda install matplotlib
    $ conda install jupyter
    $ conda install notebook
    $ conda install jupyterlab
    $ conda install ipython
    $ conda install ipykernel
    $ conda install ipywidgets        
    
    $ ipython kernel install --user --name=ccc
    Installed kernelspec ccc in /home/ofer/.local/share/jupyter/kernels/ccc

## conda:
(I installed the regular miniconda in aws ec2)    
need license           

    $ wget https://repo.anaconda.com/archive/Anaconda3-2023.09-0-Linux-x86_64.sh
    $ bash Anaconda3-2023.09-0-Linux-x86_64.sh 
    $ conda config --set auto_activate_base false
    $ conda update conda
    $ conda create -n ccc python=3.11
    $ conda activate ccc

Install the following packages:   

    $ conda install -c anaconda sympy
    $ conda install anaconda::scipy
    $ conda install conda-forge::matplotlib
    $ conda install anaconda::jupyter
    $ conda install -c conda-forge notebook
    $ conda install -c conda-forge jupyterlab
    $ conda install anaconda::ipython
    $ conda install anaconda::ipykernel
    $ conda install anaconda::ipywidgets

    $ ipython kernel install --user --name=ccc
    Installed kernelspec ccc in /home/ofer/.local/share/jupyter/kernels/ccc

