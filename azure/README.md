# Harvester Auto-installation testing
This repo aims at providing a simple iterative testing setup for Harvester auto-install configuration.
This repo exists because we cannot always get things right from the start. So, whenever someone needs to create automation for deploying a Harvester cluster, they need to expect some level of iteration. The problem is that Bare Metal infrastructure (even on a very automation-friendly cloud such as Equinix Metal) is still very slow. A Bare Metal Server typically needs multiple minutes to go through the sequence of checking memory, configuring the network for PXE, etc.

Since Harvester's installation can fail in a very early stage when using a wrong configuration, this repo simplifies this by:
- Automating the creation of a setup environment using nested virtualization
- Bootstrapping a valid minimal configuration for Harvester installation
- Offering a way to easily test multiple scenarios using QEMU for Hardware simulation
