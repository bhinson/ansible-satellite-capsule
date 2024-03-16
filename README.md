# Forked from https://github.com/RedHatSatellite/capsule-maintain

# capsule-maintain
Install/upgrade a Satellite6 Capsule server using ansible playbooks.

## Getting Started

#### What you need: ####
- Satellite 6.x version server.
- Target server(s) for Capsule installation/upgrade.
- Password-less ssh from all required capsules.
- You can run install/upgrade/update on one or more capsule servers at one time.
- Make sure that the required firewall ports are opened in your Capsule and Satellite servers.
- Activation Key / Content view with the following repos:
  * rhel-8-for-x86_64-baseos-rpms
  * rhel-8-for-x86_64-appstream-rpms
  * satellite-capsule-<capsule_version>-for-rhel-8-x86_64-rpms
  * satellite-maintenance-<capsule_version>-for-rhel-8-x86_64-rpms


#### Supported Scenarios: ####
- Capsule 6.x version installation.
- Capsule 6.x upgrade.
- Capsule z-stream update.

#### Setup ####
In `vars.yml` file, update the following parameters:
 - `capsule_version` - Version of the capsule (`6.10`,`6.11`, etc.) to be installed.
 - `satellite_org_label` - (applicable to install only) Label of the Satellite Organization to which the capsule needs to be registered.
 - `satellite_activation_key` - (applicable to install only) Activation key of the Satellite Organization to which the capsule needs to be registered.
 - `skip_katello_agent` - (applicable to install only) Set to true to not install katello-agent. (defaults to false)
