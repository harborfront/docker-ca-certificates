# harborfront/base

![Travis CI Build Status](https://travis-ci.org/harborfront/docker-ca-certificates.svg)

`FROM harborfront/base`

This is a Docker base image with builds off of the [scratch](https://hub.docker.com/r/_/scratch/) image, and adds the root certificates for all the standard certificate authorities.

This repository uses the list of root certificates accepted under the [Mozilla CA Certificate Program](https://www.mozilla.org/en-US/about/governance/policies/security-group/certs/). This set of root certificates are currently used in primarily in [Mozilla's Network Security Services (NSS)](https://developer.mozilla.org/en-US/docs/NSS). The original certificate trust source can be found [here](http://mxr.mozilla.org/mozilla-central/source/security/nss/lib/ckfw/builtins/certdata.txt).


This repository is set to automatically build monthly, so that you will get the latest updates from the Mozilla CA Certificates Program.

This repository uses the code from [agl/extract-nss-root-certs](https://github.com/agl/extract-nss-root-certs) repository, to parse the NSS Certificates file.

This image is best used for creating minimal Docker images with statically-linked Go binaries.

## Feedback &amp; Issues
For all feedback and issues, please [create a GitHub issue](https://github.com/harborfront/docker-ca-certificates/issues/new).

## License
This repository is licensed under the [Mozilla Public License version 2.0](https://github.com/harborfront/docker-ca-certificates/blob/master/LICENSE).
