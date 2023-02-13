# Github Action: pypi-build-publish

Github action to build and publish to PyPI [PEP 518](https://www.python.org/dev/peps/pep-0518/) compliant projects (flit, poetry,...).

Usage:

```yaml
- use: conchylicultor/pypi-build-publish@v1
  with:
    pypi-token: ${{ secrets.PYPI_API_TOKEN }}
```

The action assume:

* The project has a `pyproject.toml` (or `setup.py`) in the top-level directory (otherwise set `path: "./path/to/project/"`).
* Python and pip are installed (e.g. by `actions/setup-python@v2`).

## Inputs

* `pypi-token`: (required) The PyPI API token to use.
* `path`: (optional) Directory of the project (containing the `pyproject.toml`). Default to root directory.

## Outputs

None.
