# Molecule docker image

Molecule (Ansible) Docker image based on original [Ansible](https://hub.docker.com/r/dimaliv/ansible) Docker image.

## Requirements

Software:

* [Docker](https://www.docker.com/)
* [GNU Make](https://www.gnu.org/software/make/)

## Build image

To build latest Molecule version image run:

```sh
make
```

To build specific Molecule version image run:

```sh
MOLECULE_VERSION=8 make
```

Also you can set Ansible base Docker image and version:

```sh
ANSIBLE_BASE_IMAGE=namespace/molecule ANSIBLE_BASE_IMAGE_VERSION=8.0.0 make
```

## Run working container

Run:

```sh
make docker-run
```

## Licence

MIT
