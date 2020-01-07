Kubernetes Event-driven Autoscaling (KEDA)
===

**Name of project:** Kubernetes Event-driven Autoscaling

**Description:**

Deploying applications on Kubernetes has become trivial, but that's only where it begins. As a platform gains more momentum, it has to survive and adapt - Autoscaling is an important aspect to accomplish this.

While Kubernetes provides application autoscaling out-of-the-box with Horizontal Pod Autoscalers (HPA), it is sometimes too limited as it only covers resource metrics while often you want to scale on external metrics instead. In reality, that means you have to deploy 3r party metric adapters based on the system you depend on, but you can only run one in the same cluster and have to manage it.

In 2019, Kubernetes Event-driven Autoscaling (KEDA) was launched by Microsoft and Red Hat to build an open application-oriented scaling mechanism that is vendor-agnostic and acts as an external metric aggregater which allows you to use 0-to-n scaling based on a variety of external metrics for different vendors. On November 19th, 2019 KEDA v1.0 has been released which makes it production-ready and provides enterprise-grade security.

With Kubernetes Event-driven Autoscaling (KEDA) we aim to make application autoscaling super simple, regardless of the data source that you are using, by abstracting away the metric adapters and allowing KEDA customers to only focus on their scaling needs of their platform.

Customers can describe how their workloads, deployments or jobs, should scale based on the criteria and deploy it as a first-class resource on Kubernetes and that's it - Kubernetes Event-driven Autoscaling (KEDA) handles the rest.

Instead of reinventing the wheel, Kubernetes Event-driven Autoscaling (KEDA) is extending Kubernetes - When a workload has to scale from 0-to-n instances, it will automatically create an  Horizontal Pod Autoscalers (HPA) until there is no work left and it gets removed again.

Kubernetes Event-driven Autoscaling (KEDA) provides production-grade security by supporting pod identities, like Azure AD Pod Identity, to avoid secret management and allow for authentication re-use across multiple scalers. This allows existing deployments to run under the same minimal permissions while KEDA scalers can use higher-priviledged authentication to gain the required metrics. With this approach, we allow developers to focus on their workload while ops manages the authentication & configuration of the autoscaling, although it can be managed end-to-end by a full-stack as well.

**Statement on alignment with CNCF mission:**

Kubernetes Event-driven Autoscaling (KEDA)'s mission is to make application autoscaling simple allowing Kubernetes users to focus on their workloads, not the scaling infrastructure. As part of that mission, we want to support as many customers as possible by being vendor neutral and are open to scale on any system.

The Kubernetes Event-driven Autoscaling (KEDA) project does not want to reinvent the wheel but build on standards instead and is complimentary to Kubernetes. Next to that, we have support for other CNCF projects like Prometheus and NATS as well and package our product as a Helm chart (2.x & 3.x) as well which is available on Helm Hub.

While the scaling features of Kubernetes Event-driven Autoscaling (KEDA) are important, we are a strong believer of making the product itself operable as well. By using Operator SDK we also want to allow operators to efficiently manage the infrastructure necessary to run Kubernetes Event-driven Autoscaling (KEDA) and are planning to provide a better operational experience as a whole by providing a CLI, dashboard, etc.

Security is one of our main focuses and we will keep on investing in that - This is why pod identity has been one of our main focuses for 1.0 and will continue to support more identity providers over time.

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
 * Aarthi Saravanakumar (Microsoft)
 * Ahmed ElSayed (Microsoft)
 * Zbynek Roubalik (Red Hat)
 * Ben Browning (Red Hat)
 * Tom Kerkhove (Codit)

Additional Maintainers:

 *  Zach Dunton - (Smartfrog)

**Infrastructure requests (CI / CNCF Cluster):**

We do not have infrastructure requests as we've got everything already setup:

- GitHub Actions for CI/CD
- Docker images are stored on Azure Container Registry (sponsored by Microsoft)
- Helm charts are hosted on GitHub Pages

**Communication Channels:**

* IM/Slack: #keda on https://kubernetes.slack.com
* Issue tracker: https://github.com/kedacore/keda
* Mailing List: None

**Website:** https://keda.sh

**Release methodology and mechanics:**

TO BE DEFINED, depends on https://github.com/kedacore/keda/issues/439
Example:
> Continuous release process made possible by reliable automated tests.
> 
> We plan to cut small releases whenever possible.

**Social media accounts:**

 * Twitter: @kedaorg

**Existing sponsorship**: Microsoft and Red Hat

**Community size:**

TO BE DEFINED, example:
>   *Existing buildpacks:*
> 
> Cloud Foundry Buildpacks:
>   1000+ stars, 4,000+ forks, 8 full-time engineers
> 
>   Heroku Buildpacks:
>   5,500+ stars, 12,000+ forks, 5 full-time engineers
> 
>   *Cloud Native Buildpacks project:*
> 
>   New project with 10 active contributors from Pivotal and Heroku.
