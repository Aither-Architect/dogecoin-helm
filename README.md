# DogecoinD Docker Image

## ALPHA RELEASE !!!
While there's enough information around the web to get started running a Dogecoin FullNode, there isn't any central documentation for ongoing operations and maintenance of a Doge server. This repo along with dogecoin-docker aim to fill that gap over time.

## Testing and Supported K8s Platforms
Automated Helm-based tests are on the roadmap in order to scale development/support across K8s platforms/distros (EKS Support is next) For now this has been tested on a DigitalOcean Kubernetes 1.20 cluster as that's the lowest barrier of entry i've found into the k8s arena and we want this in as many hands as possible.

## CONTRIBUTING
Pull Requests are welcome! It's as simple as that for now.


## TODO -
- Back the pod's data with a volume by turning the Deployment into a StatefulSet
- Determine best practices on how to join the network
- Document procedures for upgrading/rollback outside of a k8s context
- Document all the things, really
- Establish init containers for clean startup
- Set up automated builds/testing in CircleCI
- Assess methods to reduce Initial Block Download
- Assess what is needed to evolve Dogecoin into a Cloud Native architecture for maximizing resilience and uptime

### Targeted K8s platforms:
- DigitalOcean (current effort)
- AWS/EKS (next)
- Azure/AKS