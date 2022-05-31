# DevSecOps task

## Intro

This repository contains simple Python API with three endpoints: `/hello`, `/ready` and `/alive`,
as well as a basic `Dockerfile` necessary to run the code in container.

## Main task

This task is about deploying above code in Kubernetes (>= 1.22) and providing a URL to access
`/hello` endpoint from outside the Kubernetes cluster.

Commit all the infrastructure code to this repository. Pay attention to availability, reliability
and security of the proposed solution on each layer.

## Bonus tasks

- Do the same but deploy to the `EKS` cluster. Provision all the infrastructure using `Terraform`.

- Use Kubernetes Ingress and expose API via [http://examle.internal/hello](http://examle.internal/hello).

- Prepare second deployment of `Python API` and implement `network policies` in Kubernetes in a way 
  that pods from different deployments cannot communicate with each other.

## Code quality

In order to keep a certain amount of code quality we are using pre-commit hooks
in this repository, which are installed by a 3rd-party tool called [pre-commit](https://pre-commit.com/).

Please follow [this documentation](https://pre-commit.com/#install) to install `pre-commit`
on your local machine. After that just execute the following command to install the hooks
to your git folder:

```shell
pre-commit install
```

Furthermore, this repository has GitHub Actions configured to run `pre-commit` on each `pull-request`
and push to `main` branch.
