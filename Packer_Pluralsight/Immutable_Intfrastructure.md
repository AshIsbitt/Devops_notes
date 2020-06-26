# Designing Immutable Infrastructure with Packer

Immutable - Unchanging over time

"Cats and Cattle, oh my" - A cat server is one that gets patches and patches again and again, trying to keep it alive until the last moment

Instead, you want Cow servers, machines that only do a thing, instead of being the only one alive at the time. If it goes, you just restart it with a new provision.

Cats
- kept alive at all costs
- needs manual intervention
- difficult to scale
- high stress

Cattle
- expendable
- Work out of the box
- easy to scale
- low stress

Other benefits
- Testable
- Reproduce production
- units of deployment
- confident changes

When do you use immutable structure - All the time, unless you're doing something extremely small scale.

How to create Ummutable Structure
- Docker - uses linux containers to deploy an OS within an OS
- Packer - Image-based, based off of the platform you're working with. Also cross platform.

Packer utilises native tools
- integrates with Chef
- Easy to transfer to Docker

Packer uses JSON templates, and can be edited in any text editor. 

Three main parts to any template
- Builders
- Provisioners
- Post-processors

Builders
- These generate the image, are provider specific, and with multiple builders, can be multi-platform. 

Provisioners
- These allow for image customisation, by running OS scripts, like Bash, or working with configuration management.
- These could be specific to the Builder IE querying the builder.

Post-Processors
- These are the last touches, and they aren't always needed. They can integrate with other services, and are key to Docker conversion.
- Not too useful for AWS

Script Provisioners
- Local Shell - this allows for running a bash script on your local machine, not on the remote machine
- Remote Shell - this runs on the machine that packer is building
- Powershell - this is the remote shell for windows
- Windows Shell - this is a local command for windows
- Windows Restart

Always add a -e flag in the /bin/bash
This always includes an error flag if there's an error within the packer config - it's a very useful debugging tool.

### User Variables

There is a variable section that can go above the Builders section. This is used to define variables, or refer to environment variables too

You can enter text into the variable when you run `packer build` as well.

----------

Builders can also create VMs within Virtualbox, where it will need the ISO of the various OS's already. This is a more hands-on method, and is local instead of on the cloud.

You will also need a "boot_wait" field, which will halt progression on installation for the specified time, for a previous command to run.

It's also recommended that you include a shut-down command at the end too

"headless" command is used to specify if you have the UI open when running packer. It's recommended to set this to false so that you can see what the command line is doing.

Certain provisioners can be set to run on certain environments within the packer provision.

