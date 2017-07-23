Bootstrap: docker
From: ubuntu:latest

%runscript

    echo "I can put here whatever I want to happen when the user runs my container!"
    exec echo "Hello Monsoir Meatball" "$@"

%post

   echo "Here we are installing software and other dependencies for the container!"
   apt-get update
   apt-get install wget
   wget http://repo.continuum.io/miniconda/Miniconda3-3.7.0-Linux-x86_64.sh -O ~/miniconda.sh
   bash ~/miniconda.sh -b -p /opt/miniconda
   export PATH="/opt/miniconda/bin:$PATH"   
   conda install numpy dask distributed
   
   

