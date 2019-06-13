# makisu-shell [![Build Status](https://travis-ci.org/hariyaa/makisu-shell.svg?branch=master)](https://travis-ci.org/hariyaa/makisu-shell)

Makisu is a fast and flexible Docker image build tool. It comes with an alpine image for shell access. 
You can find the source from uber/makisu github repository. makisu-shell is a simplified version of it.

Docker usage

```docker pull hariyaa/makisu-sh```

Kubernetes usage

```kubectl run makisu --image=hariyaa/makisu --restart=Never --dry-run```
