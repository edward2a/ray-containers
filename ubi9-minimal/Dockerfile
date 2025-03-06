FROM registry.access.redhat.com/ubi9-minimal

ARG PYTHON_VERSION
ARG RAY_VERSION
ARG RAY_META_PKG

RUN microdnf install -y python${PYTHON_VERSION} python${PYTHON_VERSION}-pip &&\
    microdnf clean all
RUN useradd -m -s /bin/bash -r ray

USER ray
RUN pip${PYTHON_VERSION} install --no-cache-dir ray[${RAY_META_PKG}]==${RAY_VERSION}

ENTRYPOINT ["/bin/bash"]

