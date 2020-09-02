你好！
很冒昧用这样的方式来和你沟通，如有打扰请忽略我的提交哈。我是光年实验室（gnlab.com）的HR，在招Golang开发工程师，我们是一个技术型团队，技术氛围非常好。全职和兼职都可以，不过最好是全职，工作地点杭州。
我们公司是做流量增长的，Golang负责开发SAAS平台的应用，我们做的很多应用是全新的，工作非常有挑战也很有意思，是国内很多大厂的顾问。
如果有兴趣的话加我微信：13515810775  ，也可以访问 https://gnlab.com/，联系客服转发给HR。
[![Go Report Card](https://goreportcard.com/badge/github.com/GoogleCloudPlatform/airflow-operator)](https://goreportcard.com/report/github.com/GoogleCloudPlatform/airflow-operator)

**This is not an officially supported Google product.**

## Community

* Join our [Slack channel](https://kubernetes.slack.com/messages/CC1UAMYSV).

## Project Status

*Alpha*

The Airflow Operator is still under active development and has not been extensively tested in production environment. Backward compatibility of the APIs is not guaranteed for alpha releases.

## Prerequisites
* Version >= 1.9 of Kubernetes.
* Uses 1.9 of Airflow (1.10.1+ for k8s executor)
* Uses 4.0.x of Redis (for celery operator)
* Uses 5.7 of MySQL

## Get Started

[One Click Deployment](https://console.cloud.google.com/marketplace/details/google/airflow-operator) from Google Cloud Marketplace to your [GKE cluster](https://cloud.google.com/kubernetes-engine/)

Get started quickly with the Airflow Operator using the [Quick Start Guide](https://github.com/GoogleCloudPlatform/airflow-operator/blob/master/docs/quickstart.md)

For more information check the [Design](https://github.com/GoogleCloudPlatform/airflow-operator/blob/master/docs/design.md) and detailed [User Guide](https://github.com/GoogleCloudPlatform/airflow-operator/blob/master/docs/userguide.md)

## Airflow Operator Overview
Airflow Operator is a custom [Kubernetes operator](https://coreos.com/blog/introducing-operators.html) that makes it easy to deploy and manage [Apache Airflow](https://airflow.apache.org/) on Kubernetes. Apache Airflow is a platform to programmatically author, schedule and monitor workflows. Using the Airflow Operator, an Airflow cluster is split into 2 parts represented by the `AirflowBase` and `AirflowCluster` custom resources.
The Airflow Operator performs these jobs:
* Creates and manages the necessary Kubernetes resources for an Airflow deployment.
* Updates the corresponding Kubernetes resources when the `AirflowBase` or `AirflowCluster` specification changes.
* Restores managed Kubernetes resources that are deleted.
* Supports creation of Airflow schedulers with different Executors
* Supports sharing of the `AirflowBase` across mulitple `AirflowClusters`

Checkout out the [Design](https://github.com/GoogleCloudPlatform/airflow-operator/blob/master/docs/design.md)

![Airflow Cluster](docs/airflow-cluster.png)


## Development

Refer to the [Design](https://github.com/GoogleCloudPlatform/airflow-operator/blob/master/docs/design.md) and [Development Guide](https://github.com/GoogleCloudPlatform/airflow-operator/blob/master/docs/development.md).

## Managed Airflow solution

[Google Cloud Composer](https://cloud.google.com/composer/) is a fully managed workflow orchestration service targeting customers that need a workflow manager in the cloud.
