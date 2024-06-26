# File Handling Support

The JupyterLab extension can be extended to provide additional support for handling files of various filetypes, as well as handling how files are managed.

```{warning}
The `jupyterlab-git` extension seems to confuse the environment regarding which base directory it is working in. If you get an error tryung to create a new notebook, click in to the file browser, or select a directory in the file browser to set the path.
```

## File browsing and handling

- `jupyterlab-unfold = "^0.3.0"` [[repo](https://github.com/jupyterlab-contrib/jupyterlab-unfold)]: the JupyterLab file browser is limited to displaying the files that are within a selected folder; this extensions adds a tree view to the files sidebar to provide a few over multiple directories and the files contained within them;

- `jupyter-archive = "^3.4.0"` [[repo](https://github.com/jupyterlab-contrib/jupyter-archive/)]: provides support for archiving and downloading multiple files; by default, uses the `zip` format; *this extension may be useful for students want to bundle files for submission as part of a TMA or EMA;*

- `jupyterlab-filesystem-access = "^0.6.0"` *(Chrome only)* [[repo](https://github.com/jupyterlab-contrib/jupyterlab-filesystem-access)]: provides access to the local filesystem, allowing notebooks to be accessed from, and saved to, the user's desktop, even if the Jupyter environment is remotely hosted;  *the extension allows students to persist their files on the own computer, even if using a remotely hosted VCE*. To create a new file that is shared to the remote filesystem, right-click in the file browser and create a file there rather than creating it from the launcher [[related issue](https://github.com/jupyterlab-contrib/jupyterlab-filesystem-access/issues/65), *apparently resolved*].

- `jupyterlab-git = "^0.50.0"` [[repo](https://github.com/jupyterlab/jupyterlab-git)]: allows users to manage files using git, as well as push and pull files from a remote repository (.g. GitHub); *this extension would allow students to synch files from a container, with or without persistent storage mounted into the container, with a remote git repository*;

- `jupytext = "^1.16.0"` [[docs](https://jupytext.readthedocs.io/en/latest/)]: by default, Jupyter notebooks are saved using the `.ipynb` (JSON) document format; `jupytext` provides support for saving notebooks using simple text based formats (various flavours of markdown, as Python docs, etc.). With `jupytext` installed, text format documents can be opened using the notebook editor, code can be executed within that view, etc. *Note that Jupytext does not save cell outputs into the supported text output documents.*

## Renderers

- `jupyterlab-geojson = "^3.3.1"`[[repo](https://github.com/jupyterlab/jupyter-renderers/tree/main/packages/geojson-extension)]: render GeoJSON using an interactive map; *clicking on a `.geojson` file will display it using an interactive map view*;
- `jupyter-compare-view = "^0.2.4"` [[repo](https://github.com/Octoframes/jupyter_compare_view)]: allows you to compare two images using a split view slider.
