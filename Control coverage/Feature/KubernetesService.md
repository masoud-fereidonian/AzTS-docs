## Kubernetes Service

| ControlId | Dependent Azure API(s) and Properties | Control spec-let |
|-----------|-------------------------------------|------------------|
| <b>ControlId:</b><br>Azure_KubernetesService_AuthN_Enabled_AAD<br><b>DisplayName:</b><br>AAD should be enabled in Kubernetes Service.<br><b>Description: </b><br> AAD should be enabled in Kubernetes Service. | <b> ARM API to list Container Services at subscription level: </b> <br> /subscriptions/{subscriptionId}/providers/Microsoft.ContainerService/managedClusters? <br> api-version=2020-09-01 <br><b>Properties:</b><br> properties.clientAppID <br> properties.serverAppID <br> properties.tenantID <br> properties.managed | <b>Passed: </b><br> Azure AD applications (Server App and Client App) **are configured** for Kubernetes Service for authentication of the credentials provided by the client. <br><b>Failed: </b><br>Azure AD applications (Server App and Client App) **are not configured** for Kubernetes Service for authentication of the credentials provided by the client.|
| <b>ControlId:</b><br>Azure_KubernetesService_Deploy_Enable_Cluster_RBAC<br><b>DisplayName:</b><br>Access policies on Notification Hub must not have Manage access permissions.<br><b>Description: </b><br> Access policies on Notification Hub must not have Manage access permissions. | <b> ARM API to list Container Services at subscription level: </b> <br> /subscriptions/{subscriptionId}/providers/Microsoft.ContainerService/managedClusters?api-version=2020-09-01 <br><b>Properties:</b><br> properties.enableRBAC | <b>Passed: </b><br> RBAC is enabled for AKS.<br><b>Failed: </b><br>RBAC is disabled for AKS. |