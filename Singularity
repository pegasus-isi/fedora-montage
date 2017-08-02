bootstrap: docker
From:      fedora:latest

%post

yum upgrade -y

yum groupinstall -y \
    "Development Tools" \
    "Development Libraries"

yum install -y \
    curl \
    gcc-gfortran \ 
    pkg-config \
    python \
    python-astropy \
    python-devel \
    unzip \
    vim \
    wget

yum clean all    

cd /opt && \
    wget -nv http://montage.ipac.caltech.edu/download/Montage_v5.0.tar.gz && \
    tar xzf Montage_v5.0.tar.gz && \
    rm -f Montage_v5.0.tar.gz && \
    cd Montage && \
    make
