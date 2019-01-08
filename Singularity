From:nfcore/base
Bootstrap:docker

%labels
    MAINTAINER Alexander Peltzer <alexander.peltzer@qbic.uni-tuebingen.de>
    DESCRIPTION Container image containing all requirements for the nf-core/chipseq pipeline
    VERSION 1.0dev
    
%environment
    PATH=/opt/conda/envs/nfcore-chipseq-1.4dev/bin:$PATH
    export PATH
    
%files
    environment.yml /

%post
    git clone https://github.com/nf-core/chipseq.git
    /opt/conda/bin/conda env create -f chipseq/environment.yml
    /opt/conda/bin/conda clean -a
