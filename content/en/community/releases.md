---
title: Releases
weight: -20
---

Open Cluster Management has approximately a three to four month release cycle. The current release is `v0.5.0`. Continue reading to view upcoming releases:

## `v0.6.0`, on 21st, January 2022

The Open Cluster Management team is proud to announce the release of OCM v0.6.0! We made many enhancements on core components and introduced some new addons.

- [First release of cluster-proxy addon](https://github.com/open-cluster-management-io/cluster-proxy), Cluster-Proxy addon is to provide a reverse tunnel from the managed cluster to the hub using `apiserver-network-proxy`, so user can easily visit the apiserver of the managedcluster from the hub without complicated infrstructure configuration. See [here](https://open-cluster-management.io/scenarios/pushing-kube-api-requests/) on how to use cluster-proxy in OCM.
- [First release of managed-serviceaccount addon](https://github.com/open-cluster-management-io/managed-serviceaccount), Managed-Servicesaccount addon provides a mechanism to project a service account on a managed cluster to the hub. The user can then use this projected account to visit services on the managed cluster. 
- [Sync status of applied resources in ManifestWork](https://github.com/open-cluster-management-io/enhancements/tree/main/enhancements/sig-architecture/29-manifestwork-status-feedback), The users can specify the status field of the applied resource they want to explore in the ManifestWork spec, and get results from the status of the ManifestWork. See [here](https://open-cluster-management.io/concepts/manifestwork/#fine-grained-field-values-tracking) on how to use this feature in Manifestwork.
- [Placement extensible scheduling](https://github.com/open-cluster-management-io/enhancements/blob/main/enhancements/sig-architecture/32-extensiblescheduling), a new API AddonPlacementScore is added which allows third party controllers to score the clusters based on various metrics. The user can specify what score should be used in the Placement API to select clusters.
- [Helm chart interface for addon framework](https://github.com/open-cluster-management-io/addon-framework/pull/62), a new interface is added in addon framework with which the developer can build an addon agent from a helm chart. See [example](https://github.com/open-cluster-management-io/addon-framework/tree/main/examples/helloworld_helm) on how to build an addon agent from the helm chart.
- [Placement API support for multicloud-operators-subscription](https://github.com/open-cluster-management-io/multicloud-operators-subscription/pull/55), subscription now supports Placement API and can leverage all new features in Placement API to deploy application packages.

We also added many new functions in [clusteradm](https://github.com/open-cluster-management-io/clusteradm) and enhanced the website documentation.

See details in the release changelogs::
- registration v0.6.0 [changelog](https://github.com/open-cluster-management-io/registration/blob/v0.6.0/CHANGELOG/CHANGELOG-v0.6.md)
- work v0.6.0 [changelog](https://github.com/open-cluster-management-io/work/blob/v0.6.0/CHANGELOG/CHANGELOG-v0.6.md)
- placement v0.3.0 [changelog](https://github.com/open-cluster-management-io/placement/blob/v0.3.0/CHANGELOG/CHANGELOG-v0.3.md)
- addon-framework v0.2.0 [changelog](https://github.com/open-cluster-management-io/addon-framework/blob/v0.2.0/CHANGELOG/CHANGELOG-v0.2.md)
- registration-operator v0.6.0 [changelog](https://github.com/open-cluster-management-io/registration-operator/blob/v0.6.0/CHANGELOG/CHANGELOG-v0.6.md)
- multicloud-operators-subscription v0.6.0 [changelog](https://github.com/open-cluster-management-io/multicloud-operators-subscription/blob/v0.6.0/CHANGELOG/CHANGELOG-v0.6.md)
- cluster-proxy v0.1.3 [repo](https://github.com/open-cluster-management-io/cluster-proxy)
- managed-serviceaccount v0.1.0 [repo](https://github.com/open-cluster-management-io/managed-serviceaccount)
- clusteradm v0.1.0 [changelog](https://github.com/open-cluster-management-io/clusteradm/blob/v0.1.0/CHANGELOG)
- config-policy-controller v0.6.0 [changelog](https://github.com/open-cluster-management-io/config-policy-controller/blob/main/CHANGELOG/CHANGELOG-v0.6.0.md)
- governance-policy-propagator v0.6.0 [changelog](https://github.com/open-cluster-management-io/governance-policy-propagator/blob/main/CHANGELOG/CHANGELOG-v0.6.0.md)
- governance-policy-status-sync v0.6.0 [changelog](https://github.com/open-cluster-management-io/governance-policy-status-sync/blob/main/CHANGELOG/CHANGELOG-v0.6.0%20.md)
- governance-policy-spec-sync v0.6.0 [changelog](https://github.com/open-cluster-management-io/governance-policy-spec-sync/blob/main/CHANGELOG/CHANGELOG-v0.6.0.md)
- governance-policy-template-sync v0.6.0 [changelog](https://github.com/open-cluster-management-io/governance-policy-template-sync/blob/main/CHANGELOG/CHANGELOG-v0.6.0.md)
- ocm-kustomize-generator-plugins v1.3.0 [changelog](https://github.com/open-cluster-management-io/ocm-kustomize-generator-plugins/blob/main/CHANGELOG/CHANGELOG-v1.3.0.md)

There are 20+ contributors making contributions in this release, they are @champly, @ChunxiAlexLuo, @dhaiducek, @elgnay, @haoqing0110, @ilan-pinto, @mikeshng, @morvencao, @mprahl, @nathanweatherly, @qiujian16, @rokej, @skeeey, @TheRealHaoLiu, @serngawy, @suigh, @xauthulei, @xiangjingli, @xuezhaojun, @ycyaoxdu, @yue9944882, @zhujian7, @zhiweiyin318. Thanks for your contributions!

## `v0.5.0`, on 8th, November 2021

Open Cluster Management team is proud to annouce the release of OCM v0.5.0! We made several enhancements on APIs
and addons which include:

- [Support deleteOption in ManifestWork.](https://github.com/open-cluster-management-io/enhancements/tree/main/enhancements/sig-architecture/10-deletepropagationstrategy)
- [Introduce plugin mechanism in Placement API and add resource based scheduling.](https://github.com/open-cluster-management-io/enhancements/tree/main/enhancements/sig-architecture/15-resourcebasedscheduling)
- ManagedClusterSet API is upgraded from v1alpha1 to v1beta1.
- Scalability improvement on application manager.

In addition, we also release the first version of [clusteradm](https://github.com/open-cluster-management-io/clusteradm)
to ease the installation of OCM, and [addon-framework](https://github.com/open-cluster-management-io/addon-framework) to
ease the development of management addons on OCM.

To see details of the changelogs in this release:
- registration v0.5.0 [changelog](https://github.com/open-cluster-management-io/registration/blob/v0.5.0/CHANGELOG/CHANGELOG-v0.5.md)
- work v0.5.0 [changelog](https://github.com/open-cluster-management-io/work/blob/v0.5.0/CHANGELOG/CHANGELOG-v0.5.md)
- placement v0.2.0 [changelog](https://github.com/open-cluster-management-io/placement/blob/v0.2.0/CHANGELOG/CHANGELOG-v0.2.md)
- addon-framework v0.1.0 [changelog](https://github.com/open-cluster-management-io/addon-framework/blob/v0.1.0/CHANGELOG/CHANGELOG-v0.1.md)
- registration-operator v0.5.0 [changelog](https://github.com/open-cluster-management-io/registration-operator/blob/v0.5.0/CHANGELOG/CHANGELOG-v0.5.md)
- multicloud-operators-subscription v0.5.0 [chagelog](https://github.com/open-cluster-management-io/multicloud-operators-subscription/blob/v0.5.0/CHANGELOG/CHANGELOG-v0.5.md)

There are 20+ contributors making contributions in this release, they are @elgnay, @haoqing0110, @hchenxa, @huiwq1990, @itdove, @kim-fitness, @mikeshng, @panpan0000, @philipwu08, @porridge, @qiujian16, @rokej, @skeeey, @suigh, @vincent-pli, @wzhanw, @xauthulei, @xiangjingli, @xuezhaojun, @yue9944882, @zhujian7, @zhiweiyin318. Thanks for your contributions!

## `v0.4.0` on August 2021
