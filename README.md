# AWX EE

An Execution Environment for AWX.

Main features:
- Centos Stream 9
- Python 3.12
  - ara
  - boto3
  - mitogen
  - redis
  - toml
- Ansible 2.16
- Minimal base collections installed

View the full configuration in the [execution-environment.yaml](execution-environment.yaml) file.

## Build the image locally

First, [install ansible-builder](https://ansible-builder.readthedocs.io/en/stable/installation/).

Then run the following command from the root of this repo:

```bash
$ ansible-builder build -v3 -t quay.io/influxdb/awx-ee --container-runtime=docker # Uses podman by default
```

## Build the image via CI

The Github actions configuration in this repository should work for you as well, provided that you're using that platform. Just update the secrets to reflect your chosen container repository.

