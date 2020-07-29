# Dockerfiles for building manylinux2014 non-x86\_64 wheels

For building precompiled binaries on non-x86\_64 architectures in CI
we need to ensure that all the python build dependencies have wheels already
on those platforms. Otherwise we can end up in a situation where we are trying
to build everything from source in a single job which might take far too long.
This repo contains Dockerfiles to build images to use for CI jobs that are
intendend to build wheels with precompiled binaries on aarch64, ppc64le, and
s390x (which are the platforms supported by Travis CI and the manylinux2014
docker images).

