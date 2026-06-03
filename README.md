# openshift-cluster-config

A git repository containing a GitOps structure for setting up OpenShift

## Repository Structure

The repository is organized into the following directories:

- `base/`: Contains the base configuration for the OpenShift container platform. This includes the core components and settings that are common across all environments.
- `overlays/`: Contains environment-specific configurations that override the base settings. This allows for customization for different deployment environments (e.g., development, staging, production).
- `tenant-config/`: Contains configurations specific to tenant management, including user roles, permissions, and access controls.
