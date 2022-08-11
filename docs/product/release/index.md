# Service Installer for VMware Tanzu 1.3

VMware provides a number of reference designs for deploying VMware Tanzu. The reference designs are available at [VMware Tanzu Reference Architecture Documentation](https://docs.vmware.com/en/VMware-Tanzu-Reference-Architecture/index.html). 

As an alternative to manually deploying the components in the reference designs, Service Installer for VMware Tanzu simplifies and automates the deployments. 

Service Installer uses best practices for deploying, configuring, and integrating the required Tanzu for Kubernetes Operations components, such as:

- Tanzu Kubernetes Grid
- NSX Advanced Load Balancer
- Contour, Harbor, Fluent Bit, Prometheus, Grafana (Shared services)
- Tanzu Mission Control
- Tanzu Observability
- Tanzu Service Mesh

Service Installer automates the deployment of the reference designs for Tanzu for Kubernetes Operations on the following platforms:

- Tanzu Kubernetes Grid on VMware Cloud on AWS
- Tanzu Kubernetes Grid on vSphere with NSX-T
- Tanzu Kubernetes Grid on vSphere running Virtual Distributed Switch (VDS)
- Tanzu Kubernetes Grid Service on vSphere running Virtual Distributed Switch (VDS)
- Tanzu Kubernetes Grid on AWS (with or without FIPS and STIG compliance)

## Release Notes
See the Service Installer [Release Notes](WhatsNew.md) for the following:

- A summary of what's new in this release.
- Link to download the Service Installer OVA for this release.

## Deploy Service Installer for VMware Tanzu

Before you install Service Installer, ensure that you have created a management port group in vSphere. 

1. Download the Service Installer OVA.
   See the Release Notes for the download location. 
2. Log in to vSphere Client. 
3. Go to **Actions > Deploy OVF Template** to start the OVF template deployment wizard.
   - Select the **Local file** option to upload the Service Installer OVA. 
   - Provide the required computer resources and storage details.
   - Under **Select networks**, for **Appliance Network**, select the management port group.
   - Specify the NTP server and the root password for the VM.

   After the system configuration completes, the OVA deployment begins.

4. After the deployment is completes, power on the Service Installer for the VMware Tanzu bootstrap VM.

For more information about deploying an OVA, see [Deploy an OVF or OVA Template](https://docs.vmware.com/en/VMware-vSphere/7.0/com.vmware.vsphere.vm_admin.doc/GUID-17BEDA21-43F6-41F4-8FB2-E01D275FE9B4.html)

You can access the Service Installer UI at `http://<Service-Installer-VM-IP>:8888/`.

To access the Service Installer CLI, log in over SSH. Enter `ssh root@<Service-Installer-VM-IP>`.

## Documentation
<!-- - What's new in this release: [What's New](./WhatsNew.md)./-->
Instructions to run the Service Installer for VMware Tanzu for Kubernetes Operations:

- [Deploying VMware Tanzu for Kubernetes Operations on VMware Cloud on AWS Using Service Installer for VMware Tanzu](./VMware%20Cloud%20on%20AWS%20-%20VMC/TKOonVMConAWS.md)
- [Deploying VMware Tanzu for Kubernetes Operations on vSphere with NSX-T Using Service Installer for VMware Tanzu](./vSphere%20-%20Backed%20by%20NSX-T/tkoVsphereNSXT.md)
- [Deploying VMware Tanzu for Kubernetes Operations on vSphere with vSphere Distributed Switch Using Service Installer for VMware Tanzu](./vSphere%20-%20Backed%20by%20VDS/TKGm/TKOonVsphereVDStkg.md)
- [Deploying VMware Tanzu for Kubernetes Operations on vSphere with Tanzu and vSphere Distributed Switch Using Service Installer for VMware Tanzu](./vSphere%20-%20Backed%20by%20VDS/TKGs/TKOonVsphereVDStkgs.md)
- [Deploying Tanzu Kubernetes Grid on Federal Air-gapped AWS VPC Using Service Installer for VMware Tanzu](./AWS%20-%20Federal%20Airgap/AWSFederalAirgap-DeploymentGuide.md)
- [Deploying Tanzu for Kubernetes Operations on Non Air-gapped AWS VPC Using Service Installer for VMware Tanzu](./AWS%20-%20Non%20Airgap/AWSNonAirgap-DeploymentGuide.md)
