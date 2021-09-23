1) Download anaconda for Linux 64-Bit (x86) from https://www.anaconda.com/products/individual

2) Copy it under your personal folder in ICB cluster. You should be connected to just VPN. Be sure you're not connected to the server. 

`scp <your.path.to.anaconda.installer> <your.icb.user.name>@vicb-submit-01:/home/icb/<your.icb.user.name>/`

3) Now connect to the server and go to your folder:

`cd /home/icb/<your.icb.user.name>`

4) Just run one of these codes:

`export PATH="/anaconda3/bin":$PATH`

`export TMPDIR=/home/icb/<your.icb.user.name>`

This is due to prevent a common error that was encountered before. It was solved ICB IT. You should check issue [#286 on ICB_IT](https://ascgitlab.helmholtz-muenchen.de/ICB/ICB_IT/-/issues/286).


5) Install anaconda:

`bash <anaconda.installer.with.sh.extension>`

6) Go to the folder which will contain the environments:

`cd /home/icb/<your.icb.user.name>/anaconda3/envs`

7) Create an environment here. I will just call it "myenv"

`conda create --name my-env`

8) Now initiate a shell, restart it and activate your environment. Run these lines one by one:

`conda init bash`

`exec "$SHELL`

`conda activate anaconda3/envs/my-env`

9) Now you should see (my-env) at the left side of the command prompt. This means you're in your environment and you can install your desired packages here. For example:

`conda install jupyterlab`

10) Always use a [cheat sheet](https://docs.conda.io/projects/conda/en/4.6.0/_downloads/52a95608c49671267e40c689e0bc00ca/conda-cheatsheet.pdf) to minimize headaches :)

11) Follow the [ICB IT instructions](https://ascgitlab.helmholtz-muenchen.de/ICB/ICB_IT/-/wikis/How-to-submit-jobs-in-SLURM-cluster-And-Charliecloud-Tutorial#how-to-submit-a-jupyter-lab-session-with-sbatch) to learn how to run Jupyter on cluster and connect through your browser. You can create the mentioned run_jupyter.sh and jupyter.sbatch files on /home/icb/<your.icb.user.name> by using vi editor:

#This code will create a file if a file with this specified name doesn't exist in that folder. If it does exist, it opens it. Vi editor makes handling files easier on Linux.

`vi run_jupyter.sh`

Press I to switch to insert mode. Copy and paste the code from the ICB IT page. Press exit to quit the insert mode. Save by typing `:wq`.

Do the same for jupyter.batch file and follow their instructions to run jupyter and connect to it through your browser. Make sure you specify the parameters in jupyter.batch and run_jupyter.sh according to your computational needs, environment name etc.

