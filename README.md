# reproducibility-tutorial
FOSS 2020
    1  cd /scratch
    2  df -h
    3  pwd
    4  git clonehttps://github.com/frniu/reproducibility-tutorial.git 
    5  git clone https://github.com/frniu/reproducibility-tutorial.git
    6  ls
    7  clear
    8  wget https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh
    9  bash Miniconda3-latest-Linux-x86_64.sh -b -p /opt/conda
   10  ln -s /opt/conda/pkgs/*/bin/* /bin
   11  ln -s /opt/conda/pkgs/*/lib/* /usr/lib
   12  /opt/conda/bin/conda install -c conda-forge -y jupyterlab=1.2.3
   13  /opt/conda/bin/conda install -c conda-forge -y nodejs=10.13.0
   14  /opt/conda/bin/pip install bash_kernel
   15  /opt/conda/bin/pip install ipykernel
   16  /opt/conda/bin/python3 -m bash_kernel.install
   17  clear
   18  /opt/conda/bin/conda search htseq
   19  /opt/conda/bin/conda search -c bioconda htseq
   20  /opt/conda/bin/jupyter lab --no-browser --allow-root --ip=0.0.0.0 --NotebookApp.token='' --NotebookApp.password='' --notebook-dir='/scratch/reproducibility-tutorial/'
   21  clear
   22  /opt/conda/bin/conda search -c bioconda snakemake
   23  /opt/conda/bin/conda install -c bioconda -c conda-forge -y snakemake=5.8.1
   24  ln -s /opt/conda/bin/* /bin
   25  ln -s /opt/conda/lib/* /usr/lib
   26  snakemake --version
   27  clear
   28  sudo apt-get update
   29  sudo apt-get install -y apt-transport-https ca-certificates curl gnupg-agent software-properties-common
   30  curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
   31  sudo add-apt-repository  "deb [arch=amd64] https://download.docker.com/linux/ubuntu \
 $(lsb_release -cs) \
 stable"
   32  sudo apt-get update
   33  sudo apt-get install -y docker-ce docker-ce-cli containerd.io
   34  docker run hello-world
   35  cd /scratch/reproducibility-tutorial/
   36  history >>README.md
