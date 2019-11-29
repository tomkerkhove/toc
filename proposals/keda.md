Kubernetes Event-driven Autoscaling (KEDA)
===

**Name of project:** Kubernetes Event-driven Autoscaling

**Description:**

Buildpacks are application build tools that provide a higher level of abstraction compared to Dockerfiles.
Conceived by Heroku in 2011, they establish a balance of control that reduces the operational burden on developers and supports operators who manage apps at scale.
Buildpacks ensure that apps meet security and compliance requirements without developer intervention.
They provide automated delivery of both OS-level and application-level dependency upgrades, efficiently handling day-2 app operations that are often difficult to manage with Dockerfiles.

Cloud Native Buildpacks aim to unify the buildpack ecosystems with a platform-to-buildpack contract that is well-defined and that incorporates learnings from maintaining production-grade buildpacks for years at both Pivotal and Heroku, the largest contributors to the buildpack ecosystem.

Cloud Native Buildpacks embrace modern container standards, such as the OCI image format.
They take advantage of the latest capabilities of these standards, such as remote image layer rebasing on Docker API v2 registries.

**Statement on alignment with CNCF mission:**

The Cloud Native Buildpacks project is well-aligned with the CNCF's mission statement of supporting cloud native systems.
The next generation of buildpacks will aid developers and operators in packaging applications into containers (1a), allow operators to efficiently manage the infrastructure necessary to keep application dependencies updated (1b), and be available via well-defined interfaces (1c).

The Cloud Native Buildpacks project is complimentary to other CNCF projects like Helm, Harbor, and Kubernetes.
Cloud Native Buildpacks produce OCI images that can be managed by Helm, stored in Harbor, and deployed to Kubernetes.
Additionally, the project roadmap includes creating a Kubernetes CRD controller (or alternatively, adapting Knative's https://github.com/knative/build[Build CRD]) to enable cloud builds using buildpacks.

We agree with the CNCF’s “no kingmakers” principle, and propose Cloud Native Buildpacks as an alternative to Dockerfiles for certain use cases, not as a one-size-fits-all solution for building cloud apps.

**Sponsors from TOC:** TO BE DEFINED

**Preferred maturity level:** Sandbox

**License:** MIT

**Source control:** Github (https://github.com/kedacore)

**External Dependencies:**

  * TO BE DEFINED, example: https://github.com/BurntSushi/toml[github.com/BurntSushi/toml] (MIT)

**Initial Committers:**

Founding Maintainers:

 * Jeff Hollan (Microsoft)
 * Anirudh Garg (Microsoft)
 * Aarthi (Microsoft)
 * Ahmed ElSayed (Microsoft)
 * Zbynek Roubalik (Red Hat)
 * Ben (Red Hat)
 * Tom Kerkhove (Codit)

Additional Maintainers:

 * zach-dunton-sf - https://github.com/zach-dunton-sf

**Infrastructure requests (CI / CNCF Cluster):**

*Development needs:*

TO BE DEFINED, example:
  We currently use Travis for CI, but we may want to use CNCF resources to deploy Concourse CI.
  Additionally, we will need access to all common Docker registry implementations for performance and compatibility testing.
  This includes deploying Harbor to CNCF infrastructure as well as access to DockerHub, GCR, ACR, ECR, etc.

*Production needs:*

TO BE DEFINED, example:
  Additionally, we would like to use CNCF resources to host a buildpack registry containing buildpacks and buildpack dependencies.

**Communication Channels:**

* Issue tracker: https://github.com/kedacore/keda

TO BE DEFINED, example:
 * IM/Slack: https://buildpacks.slack.com
 * Mailing List: https://lists.cncf.io/g/cncf-buildpacks (proposed)

**Website:** https://keda.sh

**Release methodology and mechanics:**

TO BE DEFINED, example:
  Continuous release process made possible by reliable automated tests.

  We plan to cut small releases whenever possible.

**Social media accounts:**

 * Twitter: @kedaorg

**Existing sponsorship**: Microsoft and Red Hat

**Community size:**

TO BE DEFINED, example:
  *Existing buildpacks:*

  Cloud Foundry Buildpacks:
  1000+ stars, 4,000+ forks, 8 full-time engineers

  Heroku Buildpacks:
  5,500+ stars, 12,000+ forks, 5 full-time engineers

  *Cloud Native Buildpacks project:*

  New project with 10 active contributors from Pivotal and Heroku.