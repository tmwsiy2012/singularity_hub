Bootstrap: docker
From: ubuntu:latest

%runscript

    echo "I can put here whatever I want to happen when the user runs my container!"
    exec echo "Hello Monsoir Meatball" "$@"

%post

   echo "Here we are installing software and other dependencies for the container!"
   apt-get update
   apt-get install python-pip -y
   apt-get install python-numpy -y
   pip install dask distributed --upgrade

