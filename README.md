# Argo-CD 
#overview

argo Cd is a declarative continuous delivery tool for kubernetes. It can be used as a standalone tool or as a part of ci/cd workflow to deliver needed resources to cluster.


In order to manage infra and application configuration aligned with gitops , git repo must be single source of truth.


#argo cd with openshift


argo cd can be implemented to deliver global customer resources from a git repo to openshift cluster. These resources can contain application definition, configuration and target state for environment what can also be version controlled with argo cd.


##########

use cases of argo cd :

***sync with secret manager:

 keep openshift secrets in sync with a secret manager like valut

 *** Detect configuration drift:

 have openshift gitops detect and display a warning when cluster configuration are not in sync with the designated git repo

 **multiple clusters in one registry:

 define multiple openshift cluster configuration in  a single git repo and apply to clusters selectively, so that all cluster config are coming from a single source of truth



 **** cluster configuration hierarchy(inheritance):
Define a hierarchy of cluster configuration (stage, production, app portfolio, etc with inheritance) in a git repository, so that configuration can be applied to a single or multiple kuberenetes clusters.

***Templating and overriding configuration::
override a subset of inherited configuration and their values, so that configuration can be adjusted for the specific clusters they are being applied to
 
