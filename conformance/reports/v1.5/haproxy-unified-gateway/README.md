# HAProxy Unified Gateway

[HAProxy Unified Gateway](https://github.com/haproxytech/haproxy-unified-gateway) is the official Gateway API implementation from [HAProxy Technologies](https://www.haproxy.com).
For installation and configuration, see the [HAProxy Unified Gateway documentation](https://www.haproxy.com/documentation/haproxy-unified-gateway/).

## Table of contents

| API channel | Implementation version | Mode | Report |
|-------------|------------------------|------|--------|
| experimental | [v1.0.7](https://github.com/haproxytech/haproxy-unified-gateway/releases/tag/v1.0.7) | default | [v1.0.7 report](./experimental-v1.0.7-default-report.yaml) |

## Reproduce

The following steps reproduce the HAProxy Unified Gateway `v1.0.7` conformance test report.

1. Pull the released controller image:

    ```bash
    docker pull haproxytech/haproxy-unified-gateway:1.0.7
    ```

1. Create a Kind cluster and deploy the prerequisites:

    ```bash
    task conformance-create-ci
    ```

1. Build and load the conformance test image:

    ```bash
    task conformance-build-test-image
    ```

1. Run the suite as an in-cluster Job, reporting version `v1.0.7`:

    ```bash
    task conformance-run-job
    ```

1. The suite writes `conformance-report.yaml`, which is published here verbatim.

## Contact

- https://github.com/haproxytech/haproxy-unified-gateway/issues
