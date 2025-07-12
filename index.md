# Contributing capabilities to the Rubin Science Platform

```{abstract}
The Rubin Science Platform is a coherent ecosystem of integrated services operated (and in most cases developed) by the Data Services division of Rubin Data Management.

It is possible for second-party (wider Rubin, beyond Data Services) and third-party (external groups) to contribute capabilities for the benefit of all Rubin Science Platform users.

This document outlines the policies and process for such contributions specifically as it relates to Rubin's flagship deployment for data rights holders at data.lsst.cloud
```

```{note}
This document is correct but incomplete.
```

## Context

The Rubin Science Platform offers an opportunity to grow the capabilities it offers to its users through contributions beyond those that can be developed by the Data Services group. Doing so is consistent with our aspirations for the future of the Platform, and we are open to such proposals.

However, while it is technically possible (and may even be easy) to add to the capabilities of the Rubin Science Platform in this way, there is a tension between the benefits of such additions and:

* increasing the operational burden on the Data Services division
* increasing user support burden on the Community Science Team
* maintaining a high level of user experience
* additional impact on available resources
* segmenting the integrated philosophy of the platform (eg UI and API equivalence)

This means that we need to evaluate potential contributions against the potential opportunity costs.

We strive for transparency and demonstrable fairness as to how decisions to include capabilities (be they services, software packages, or simply datasets).
For example, hosting a dataset for a collaboration a Rubin scientist participates in must be evaluated similarly to one where they don’t.

Finally, a contributed package is likely to be removed if it fails to adhere to (possibly evolving) technical requirements, which would negatively impact users who came to rely on it.
To avoid this, potential contributors should carefully review this document prior to proposing a contribution.

## Inclusion criteria

Requests by third parties to contribute capabilities to the RSP must be first approved for consideration by the Rubin Operations Product Owner (_Leanne Guy_). Approval criteria include:

* General usefulness beyond the requestor's research group
* Determination that project resources are appropriately diverted to this capability
* Assessment of any a priori concerns over the requestor's ability to fulfill their on-going responsibilities
* Evaluation of the capability’s anticipated lifespan and/or timeliness.

The Rubin Operations Product Owner will additionally indicate to the Data Services Lead the level of priority for subsequent technical evaluation.

The Data Services lead (_Frossie Economou_) will perform a technical evaluation in conjunction with relevant RSP Product Owner(s) and Data Services engineers. Criteria include:

* Impact on resources, performance and security of the platform
* Alignment of the capability with existing or planned RSP capabilities.
* Technical soundness of the implementation.
* Open source licensing of all software assets

The technical evaluation will inform the Rubin Operations Product Owner's final decision.

In the event of approval, a formal letter (MOU) will be required from a leadership figure with oversight of the contributor (institutional director, department head or collaborator chair).
The signatory will confirm that:

* They approve of the contribution
* They confirm that the contributor(s) are authorized, able and willing to fulfill the on-going responsibilities outlined in this document
* They are aware that the capability may be withdrawn under circumstances described in this document

This formality helps mitigate the risks associated with pertinent but under-resourced contributions.```

## Post-approval process

### Delivery

As part of the delivery of software and services (but not data), the contributor is expected to:

* supply a manifest of all materials required by the capability
    * for software this includes a packaged version (eg conda package)
    * for services this means deployment with [Phalanx](https://phalanx.lsst.io)
* supply at least two notebooks that work on the RSP Notebook service
    * one that demonstrates most useful features and capabilities of the package (for our monitoring/CI system)
    * one that does a single simple (but randomized) access to the data (for scale testing)

As part of any delivery (software, services or data), the contributor is expected to:

* provide a link to externally (to the RSP) hosted documentation
* identify one or more GitHub repositories containing all code involved licensed under a major open source license
* engage in a discussion on how assets (eg. files) are best hosted (S3, POSIX etc)
* work with Data Services to minimize POSIX usage to the extent possible
* supply contact information for a minimum of two people who assume the on-going support responsibilities
* work with the Data Services Lead on a Delivery Note (a technote capturing what code, date etc is part  of the delivery)

When the delivery is complete:

* The contributor(s) will co-ordinate the Data Services regarding release (including timing of any sneak release, soft release, official release, beta-testing language, etc).
* The first formal announcement to the user community of the availability of this capability _must_ come from the project.

### Ongoing responsibilities

The same level of attention that goes into operation and maintaining Data Services' first-party capabilities is expected from contributed capabilities.

This list is likely to evolve with further developments of the platform.
The SQuaRE team in the Data Services group operates the Rubin Science Platform at data.lsst.cloud and is the final authority on this list.

* Contributors need to keep their codebases up to date, including up-revving their dependencies in a timely manner, and/or processing the PRs from our automated dependency manager as appropriate.
* Services may be asked to instrument for run-time metrics.
* A contributor may be asked to send a representative to SQuaRE's "Patch Thursday" call if the need arises.
* Any incompatibilities between contributed code and the RSP services and infrastructure needs to be resolved in a timely manner. This may require significant changes such as upgrading to a new major version of Python.
* Services must pass scale-testing benchmarks
* Contributors must attend to questions on their contribution in the [Community Forum](https://community.lsst.org) in a prompt and courteous manner.
* Contributors must attend any monitoring of their service (if applicable) and/or respond to service quality alerts they are tagged on


## Exclusion criteria

Failure to consistently meet the ongoing responsibilities outlined above *will* result in the removal of the capability.

Additionally, a capability may be withdrawn if the criteria for its inclusion no longer apply.

Finally, depending on specific circumstances, a capability may be withdrawn if it is poorly received or ignored by our user community, or if its contributors violate our [Acceptable Use Policy](https://data.lsst.cloud/terms).

## Second-party contributions

Groups within Rubin but outside Data Services (eg EPO) are considered second party contributors.
These have to follow the same guidelines, except for:

* they can apply directly to the Data Services Lead for evaluation (who will escalate to the Rubin Operations Product Owner if necessary)
* no MOU is required
* they may be asked to integrate with the [RSP documentation](https://rsp.lsst.io) instead of hosting their own

All the post-approval requirements are the same.

Note that IDACs are not second-parties in the context of the document.

