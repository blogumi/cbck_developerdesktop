# Tj testing Packer and stuff

## Usage Scenario

1. Run from local machine, spins up AMI, SSH from local machine to AMI and installs ansible, runs ansible playbook on the AMI machine
2. Run from AWS bootstrapped node, spins up AMI, SSH from bootstrap node to AMI and installs ansible, runs ansible playbook on the AMI machine

## Start Building

```Build using environment variables
packer build -var-file=./packer-base-ami/variables/snapshot.json ./packer-base-ami/packer.json
```

## Env Variables

In the variables folder create at least two files.
* snapshot.json
* release.json

Snapshots are development artificats. Can be built from anywhere. Releases are stable versions. 

### Skunkworks Notes

Ubuntu 16 filter:         "name": "ubuntu/images/*ubuntu-xenial-16.04-amd64-server-*",
