Bootstrap: docker
From: ubuntu:latest

%runscript

    echo "I can put here whatever I want to happen when the user runs my container!"
    exec echo "Hello Monsoir Meatball" "$@"

%post

   echo "Install Anaconda3 with numpy and dask distributed to /opt/miniconda3"
   apt-get update
   apt-get install wget bzip2 -y
   wget https://repo.continuum.io/archive/Anaconda3-4.4.0-Linux-x86_64.sh -O ~/miniconda3.sh
   bash ~/miniconda3.sh -b -p /opt/miniconda3
   echo 'export PATH="/opt/miniconda3/bin:$PATH"' >> /root/.bashrc
   echo 'source /opt/miniconda3/bin/activate' >> /root/.bashrc
   export PATH="/opt/miniconda3/bin:$PATH"   
   conda install numpy dask distributed 
   rm -rf ~/miniconda3.sh
   
   

