# flux-root

This repository is my personal 'flux-root', and reconciles all the Kubernetes manifests
and Helm charts that are unique to my personal projects. 

## yellowstonedev/flux-root

This repository is being reconciled by yellowstone/flux-root. Yellow Stone Dev
is an organization that my buddy and I maintain as a shared personal project.

While that code is private, its main job is to enable multi-tenancy on a shared
Kubernetes cluster hosted in Linode. That way we can both use the shared cluster
in a relatively independent manner.

The k8s flux installation is pointed to yellowstonedev/flux-root, which points
to a few other tenants, such as this repository, as well as
yellowstonedev/flux-infra-root.

yellowstonedev/flux-infra-root is where things like cert-manager and
github-actions-controller are deployed so that we can run GitHub CI pipelines
and protect our websites with TLS.

## Hosted

This repo is the source of desired state for my self-hosted Ghost blog at
[https://josh.sizer.dev](https://josh.sizer.dev). Notably, there is also a
[CronJob](https://github.com/joshsizer/flux-root/blob/main/linode/ystonedev/us-east/green/tenants/blogposts-generator.yaml?ref=josh.sizer.dev)
that runs a script that generates blogposts using ChatGPT.
