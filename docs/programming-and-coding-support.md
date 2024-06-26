# Programming and Coding Support

The following extensions are installed to support code development in notebook code cells.

## Execution monitoring

- `jupyterlab_execute_time = "^3.1.2"` [[docs](https://github.com/deshaw/jupyterlab-execute-time)]: cell status report providing the time cell was last executed, and the amount of time the cell took to execute;

![JupyterLab execution time : time of execution, and time taken to execute, displayed as cell output report](images/jupyterlab-execute-time.png)

## Code formatting

Various tools are included to support code formatting:

- `jupyterlab-code-formatter = "^2.2.1"` [[docs](https://jupyterlab-code-formatter.readthedocs.io/usage.html)]: apply code formatting to selected cell or all cells. The extension is preconfigured to work with the following packages, which as are also pre-installed into the JupyterLab environment:
  - `black = "^24.4.2" # code formatting`
  - `isort = "^5.13.2" # package import sorting`

## Autocomplete

By default, JupyterLab code cell editor includes a limited amount of tab completion support. More comprehensive support for a wide range of languages (including Python, R, and JavaScript) can be provided through the use of a language server.

- `jupyterlab-lsp = "^5.1.0"` [[repo](https://github.com/jupyter-lsp/jupyterlab-lsp)]: language server protocol extension, can be used to add in code completion hints provided by a language server; *note that as it stands, this extension is essentially redundant as no language server is installed by default in the environment;*

The following extension is *not* installed but is undergoing evaluation:

- `jupyter-ai` [[docs](https://github.com/jupyterlab/jupyter-ai)]: provides generative AI features as part of the JupyterLab user interface using local or remote models.
