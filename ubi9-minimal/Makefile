PYTHON_VERSION = '3.12'
RAY_VERSION = '2.43.0'
RAY_META_PKG = 'default'
REGISTRY = docker.io/edward2a

.PHONY: help

default:
	@echo 'Make what??'

help:
	@echo 'Not today...'

ray:
	docker build -t ${REGISTRY}/ray-${RAY_META_PKG}:${RAY_VERSION}-ubi9m --build-arg PYTHON_VERSION=${PYTHON_VERSION} --build-arg RAY_VERSION=${RAY_VERSION} --build-arg RAY_META_PKG=${RAY_META_PKG} -f Dockerfile .

