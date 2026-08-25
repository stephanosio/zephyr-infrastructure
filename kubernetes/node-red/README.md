# node-red

The `node-red` component provides the Node-RED instance deployment
configurations for automating 

Note that this component is not automatically deployed through Terraform and
must be manually deployed in the following order:

1. `configmap.yaml`
2. `pvc.yaml`
3. `deployment.yaml`
4. `service.yaml`
5. `ingress.yaml`

The admin user password hash in the `configmap.yaml` file is intentionally left
blank, and applying this manifest file as-is will result in the admin user
password hash being cleared.
