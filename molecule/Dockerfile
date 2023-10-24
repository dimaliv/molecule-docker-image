ARG BUILDKIT_INLINE_CACHE
ARG ANSIBLE_BASE_IMAGE
ARG ANSIBLE_BASE_IMAGE_VERSION

FROM ${ANSIBLE_BASE_IMAGE}:${ANSIBLE_BASE_IMAGE_VERSION}
ARG MOLECULE_VERSION
RUN apk --no-cache add docker  && \
    pip3 install --no-cache-dir \
        molecule-plugins[docker] && \
    if [[ -z "${MOLECULE_VERSION}" ]]; then \
        pip3 install --no-cache-dir molecule; \
    else \
        pip3 install --no-cache-dir molecule==${MOLECULE_VERSION}; \
    fi
CMD [ "molecule", "--version" ]
