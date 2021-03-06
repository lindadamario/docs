# Prepare Your Environment

## Install and Configure the AWS Cli tools

[Install the AWS Cli tools using this guide ](https://docs.aws.amazon.com/cli/latest/userguide/installing.html)and configure a profile:

```bash
$ aws configure --profile myproject
```

Check [this guide](https://docs.aws.amazon.com/cli/latest/userguide/cli-chap-getting-started.html) for more information on configuring AWS Cli.

Export your AWS profile to an environment variable. This variable is used by CXCloud tools to interact with your AWS account:

```bash
$ export AWS_PROFILE=myproject
```

## Install Kubernetes and Kops

Before you start, you need to have Kubernetes and it's tools installed on your computer. Follow [this guide](https://kubernetes.io/docs/tasks/tools/install-kubectl/) to Install those. On Mac, you can install Kubernetes tools using `homebrew`:

```bash
$ brew install kubernetes-cli
```

CXCloud cli uses Kops to create and configure your Kubernetes cluster. You can install it on your Mac using `homebrew`: 

```bash
$ brew update && brew install kops
```

Or on your Linux machine:

```bash
curl -LO https://github.com/kubernetes/kops/releases/download/$(curl -s https://api.github.com/repos/kubernetes/kops/releases/latest | grep tag_name | cut -d '"' -f 4)/kops-linux-amd64
chmod +x kops-linux-amd64
sudo mv kops-linux-amd64 /usr/local/bin/kops
```

Check [Kops' documentation](https://github.com/kubernetes/kops#installing) for more information.

## Install Helm

[Install the Helm client](https://docs.helm.sh/using_helm/#installing-helm) or your machine. On Mac this can be done using `homebrew`:

```bash
$ brew install kubernetes-helm
```

## Install Node.js and NPM

You need to install Node.js and NPM on your computer. It is recommended to install the latest Node.js LTS version. On macOS you can do this using `homebrew`:

```text
$ brew install node
```

For other systems, you can check [Node.js official documentation](https://nodejs.org/en/download/package-manager/).

