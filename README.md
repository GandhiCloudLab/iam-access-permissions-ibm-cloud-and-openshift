# IAM Access permssions between IBM Cloud and Managed Openshift

In IBM Cloud, the IAM users can have Viewer, Editor and Administrator permissions. Based on this permission the managed openshift allows IAM users to access the cluster.

This document explains the mapping between IAM roles and its authorization in Openshift.

Here are the IAM roles.

```
    Administrator
    Editor
    Operator
    Viewer
```

# Access rights summary

| IAM Role| View all projects and its content | Rights to create New Project | Rights to create other objects like create POD |
| -------------         | -------------                 |-------------              |------------- |
| Administrator   | Yes | Yes | Yes |
| Editor          | Yes | No | Yes |
| Viewer          | Yes | No | No |


# 1. Administrator

Administrator rights been set to the user like the below in the cluster.

<img src="images/01-Admin-Permission.png" width="900" title="Issue" bordercolor=green>
<img src="images/02-Admin-Permission2.png" width="900" title="Issue" bordercolor=green>

The user can able to Create Projects and PODS. 

<img src="images/03-Admin-CreateProject.png" width="900" title="Issue" bordercolor=green>
<img src="images/04-Admin-CreatePOD.png" width="900" title="Issue" bordercolor=green>


# 2. Editor

Editor rights been set to the user like the below in the cluster.

<img src="images/05-Editor-Permission.png" width="900" title="Issue" bordercolor=green>

The user can't to Create Projects but he can create PODS. 

<img src="images/06-Editor-CreateProject.png" width="900" title="Issue" bordercolor=green>
<img src="images/07-Editor-CreatePOD.png" width="900" title="Issue" bordercolor=green>


# 3. Viewer

Viewer rights been set to the user like the below in the cluster.

<img src="images/08-Viewer-Permission.png" width="900" title="Issue" bordercolor=green>

The user can't to Create both Projects and PODS. 

<img src="images/09-Viewer-CreateProject.png" width="900" title="Issue" bordercolor=green>
<img src="images/10-Viewer-CreatePOD.png" width="900" title="Issue" bordercolor=green>



# Note

To test the access rights, after changing the access rights in IAM do the following steps in sequence otherwise, the changes will not reflect.

1. Logout `cloud.ibm.com` website from the browser
2. Then Logout `Openshift web console` from the browser 



## General

| Topic                 | Sub Topic                     |Link                       | Last Updated| 
| -------------         | -------------                 |-------------              |------------- |
|                   |  |                              |  |

