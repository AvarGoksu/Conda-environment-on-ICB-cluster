1) Download anaconda for Linux 64-Bit (x86) from https://www.anaconda.com/products/individual

2) Copy it under your personal folder in ICB cluster. You should be connected to just VPN. Be sure you're not connected to the server. 
scp <your.path.to.anaconda.installer> <your.icb.user.name>@vicb-submit-01:/home/icb/<your.icb.user.name>/

3) Now connect to the server and go to your folder:
cd /home/icb/<your.icb.user.name>

4) Just run one of these codes:
export PATH="/anaconda3/bin":$PATH
export TMPDIR=/home/icb/<your.icb.user.name>

This is due to prevent a common error that was encountered before. It was solved ICB IT. You should check issue #286 o ICB_IT.

5) Install anaconda:
bash <anaconda.installer.with.sh.extension>

6) Go to the folder which will contain the environments:
cd /home/icb/<your.icb.user.name>/anaconda3/envs

7) Create an environment here. I will just call it "myenv"
conda create --name myenv

8) Now initiate a shell, restart it and activate your environment. Run these lines one by one:
conda init bash
exec "$SHELL"
conda activate anaconda3/envs/myenv

9) Now you should see (myenv) at the left side of the command prompt. This means you're in your environment and you can install your desired packages here. For example:
conda install jupyterlab

10) Always use a cheat sheet to minimize headaches:
https://docs.conda.io/projects/conda/en/4.6.0/_downloads/52a95608c49671267e40c689e0bc00ca/conda-cheatsheet.pdf
