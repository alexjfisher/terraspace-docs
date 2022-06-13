---
title: Terraspace Summary Command
---

The `terraspace summary` command shows a summary of all the resources grouped by statefile. This can be quite useful to help keep track of resources created by the different statefiles.

## Example

The summary is based on the statefiles in the bucket, regardless of whether or not the stack is defined in the project.

    $ terraspace summary
    Summary of resources based on backend storage statefiles
    Downloading statefiles to /tmp/terraspace/statefiles/terraform-state-111111111111-us-west-2-dev/us-west-2/dev/
    modules/instance/terraform.tfstate
        aws_ami ubuntu: ubuntu/images/hvm-ssd/ubuntu-trusty-14.04-amd64-server-20191107
        aws_instance web: i-074dcbc68f1cadc30
    modules/security-group/terraform.tfstate
        aws_security_group allow_tls: first-buck
        random_pet this: first-buck
    $

## Considerations

* The summary command is supported for aws, google, and azure only. IE: It is not supported for local backends or TFC.
* It download all statefiles for the specific TS_ENV. For performance, it requires `:ENV` to be the "containing folder" for all the state files. IE: The default backend.tf `:TYPE_DIR/:APP/:ROLE/:MOD_NAME/:ENV/:EXTRA/:REGION/terraform.tfstate` works.

## All Show Command

The `terraspace all show` command can also be helpful. It downloads `app/stacks` statefiles and and summarizes:

    $ terraspace all show
    Running:
       terraspace show demo       # batch 1
    Batch Run 1:
    Running: terraspace show demo Logs: log/show/demo.log
    terraspace show demo: Resources: 2 Outputs: 1
    Time took: 2s
    $

This command supports all backends.
