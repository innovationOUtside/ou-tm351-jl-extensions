# Managing JupyterLab Extensions on the Command Line

In the containers built using the OU container builder, the Jupyterlab environment is isolated from the notebook kernel environments.

Specifically, JupyterLab environment can accessed using the path:

`/var/lib/ou/python/system/bin/jupyter`

To view the currently installed extensions:

`/var/lib/ou/python/system/bin/jupyter labextension list`

By default in an OU VCE, the permissions with which extensions are into the JupyterLab environment as part of a system build step do not allow users to update, disable or uninstall the extension.

For example, a user attempting to run `jupyter labextension disable jupyterlab-execute-time` will be greeted with a *Permission denied* error message.

Users running a local VCE container have rather more flexibility and can login as `root` which gives them permissions to run `jupyter lab` commands from the command-line as required.

The local container can also be modified to provide the user with permissions to enable/disable extensions from the JupoyterLab extensions sidebar:

Looking at jupyterlab extensions, setting the following permissions (from `root`) seems to allow uses to control enabling / disabling extensions:

`chown ou:users /var/lib/ou/python/system/etc/jupyter/labconfig/page_config.json`

*This permission setting can be built into the hosted VCE to allow students to enable/diable ectension settings during a session, but any changes the students make to the environment will not be persisted to other sessions.*