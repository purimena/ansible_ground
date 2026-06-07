# ee-builder-test

test

## What's included

### Ansible collections

| Collection | Version | Source |
|---|---|---|
| ansible.netcommon | - | Private Automation Hub (community) |
| ansible.posix | - | Private Automation Hub (community) |
| ansible.utils | - | Private Automation Hub (community) |
| community.general | - | Private Automation Hub (community) |



## Details

- **Tags:** `execution-environment`

- **Image registry:** `aap.lab.holtit-home.com/ee-builder-test:latest`

## Use this execution environment

If your EE uses collections from private sources (Automation Hub, private automation hub), update the token settings in `ansible.cfg` before building.


Log in to the registry and pull the image:

```bash
podman login aap.lab.holtit-home.com
podman pull aap.lab.holtit-home.com/ee-builder-test:latest
```

If the registry uses a self-signed certificate, you may need to append `--tls-verify=false` to each `podman` command.

To use it in Ansible Automation Platform:

1. Go to **Automation Execution** > **Infrastructure** > **Execution Environments**.
2. Click **Create execution environment** and enter the image URL: `aap.lab.holtit-home.com/ee-builder-test:latest`
3. Select this execution environment in your job templates.

## Build details

- **Base image:** `registry.redhat.io/ansible-automation-platform/ee-minimal-rhel8:2.18`
- **Definition file:** `ee-builder-test.yml`
- **Template file:** `ee-builder-test-template.yml` - import this into Ansible automation portal to let others create EEs from the same starting point.

To make changes, use this EE's template in Ansible automation portal or rebuild manually with `ansible-builder` and the definition file.
