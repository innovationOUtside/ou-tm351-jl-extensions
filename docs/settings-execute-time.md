# Execute time

This extension can report the time at which a cell was executed, as well as the execution time itself.

The extension can be configured to only report on cell execution times that exceed a minimum specified duration.

The extension is preinstalled, but the recommemdation it to disable it by default, or only display reports for long cell execution times.

- in `.jupyter/lab/user-settings/jupyterlab-execute-time/settings.jupyterlab-settings`:

```json
{
    "enabled": false,
    "highlight": false,
    "minTime": 3,
    "showLiveExecutionTime": false,
    "showDate": true
}
```
