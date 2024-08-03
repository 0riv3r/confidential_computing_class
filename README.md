# confidential_computing_class
my code for the academic confidential computing class

## Python environments
For notebooks/ use the 'ccc' conda environment. See notebooks\README.md.     
For mpc_demo/ use the 'crypten' conda environment. See mpc_demo\README.md.                

## Setup port forwarding on the local machine
Remote notebook server (when jupyter run on ec2 for instance)    

Access notebook from remote machine over SSH by setting up a SSH tunnel.   
Run the following command from your local machine:   

    $ ssh -L 8889:localhost:<PORT> <REMOTE_USER>@<REMOTE_HOST>

    C:\Users\orivlin>ssh -i C:\Users\orivlin\.ssh\aws_rsa_ccc.pem -L 8889:localhost:8888 ubuntu@ec2-34-249-14-104.eu-west-1.compute.amazonaws.com

# Replace <PORT> with the port number you selected in the above step (8888)
# Replace <REMOTE_USER> with the remote server username
# Replace <REMOTE_HOST> with your remote server address

# Launch jupyter notebook and select the installed kernel of this virtual environment
# if the virtual-env or conda kernel is called 'ccc', select the 'ccc' kernel from the kernels dropdown
    $ cd notebooks
    $ jupyter lab  --no-browser

Open a browser from your local machine and navigate to    
http://localhost:8889/    

with the generated token.    
http://127.0.0.1:8889/?token=70cd8228e71b591a99a103a237e1e325be64b08eb3a0fecb   

Replace 8889 with your port number used in step 1.   

Or paste the jupyter token in the elocal browser when requested.   
