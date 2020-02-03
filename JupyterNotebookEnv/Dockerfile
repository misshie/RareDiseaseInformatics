FROM python:3.6-slim

RUN pip3 install -U pip wheel setuptools && \
    pip3 install \
    bash_kernel \
    jupyter && \
    python3 -m bash_kernel.install

WORKDIR /mount
ENTRYPOINT ["jupyter", "notebook"]
CMD ["--port=8888", "--ip=0.0.0.0", "--allow-root", "--notebook-dir=/mount"]
