# DogecoinD Helm Chart

This is a [Helm Chart](https://helm.sh/) to deploy a dogecoind full node into a [Kubernetes](https://kubernetes.io/) cluster. This chart is designed specifically with [this Docker image](https://github.com/Aither-Architect/dogecoin-docker) in mind, which is a multi-arch image supporting:
- x86_64
- arm64 / armv8 / aarch64

If you deploy Kubernetes to an arm64 device using [K3s](https://k3s.io/), you can install this chart in the same manner as you would an x86_64 machine:

1) `git clone git@github.com:Aither-Architect/dogecoin-helm.git`
2) `cd dogecoin-helm`
3) Adjust the `values.yaml` file to suit your needs
4) `helm install dogecoin .`

The accompanying docker image should auto-detect the cpu architecture and use the appropriate dogecoin binary.

## EXPERIMENTAL
This chart is undergoing active development and will have more features exposed over time. While there's enough information around the web to get started running a Dogecoin FullNode, there isn't any central documentation for ongoing operations and maintenance of a Doge server. This repo along with [dogecoin-docker](https://github.com/Aither-Architect/dogecoin-docker) aim to fill that gap over time.

## CONTRIBUTING
Pull requests are welcome! Just fork the repo and cut a branch with a semantic name. Make your changes and then cut a PR back here to the `main` branch.

### Targeted K8s platforms (for now):
- AWS/EKS (next)
- DigitalOcean
- Raspberry Pi 4 Model B running K3s
- 
## TODO -
- Back the pod's data with a volume by turning the Deployment into a StatefulSet
- Determine best practices on how to join the network, dns-wise
- Document procedures for upgrading/rollback
- Document all the things, really
- Establish init containers for clean startup as well as downloading the bootstrap torrent
- Set up automated testing in CircleCI
- Assess what is needed to evolve Dogecoin into a Cloud Native architecture to cultivate opportunities for features

