# hash:sha256:4b2b8e62768238f9a4d0fb408f74d4ad8fa8eae918ce16c0e42e6aee369f6765
FROM registry.codeocean.com/codeocean/miniconda3:4.9.2-python3.8-ubuntu20.04

ARG DEBIAN_FRONTEND=noninteractive

RUN conda install -y \
        ipympl==0.7.0 \
        jupyter==1.0.0 \
        jupyterlab==3.2.1 \
        matplotlib==3.4.3 \
        numpy==1.21.2 \
        pandas==1.3.4 \
        pyyaml==6.0 \
        scipy==1.7.1 \
    && conda clean -ya

RUN pip3 install -U --no-cache-dir \
    ipynb==0.5.1 \
    mag-manip==3.0.0 \
    pyibex==1.9.2 \
    pyinterval==1.2.0

COPY postInstall /
RUN /postInstall
