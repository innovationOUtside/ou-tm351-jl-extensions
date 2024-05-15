# JuptyterLab App settings

The Jupyterlab app has the ability to post alerts, for example to notify the user that an update is available.

Suppress alerts by setting the following in `.jupyter/lab/user-settings/@jupyterlab/apputils-extension/notification.jupyterlab-settings`:

```json
{
    "checkForUpdates": false,
    "doNotDisturbMode": false,
    "fetchNews": "none"
}
```