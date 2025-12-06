# **llmmd2pdf Dev Reminders**

Find the latest general documentation [here](./index.md).

## Building a New Release

1. **Ensure all tests pass**: Run your test suite to confirm everything is functioning correctly (`pytest` is recommended):
2. **Update Version**: Increment the version number in `pyproject.toml` and `__init__.py`.
3. **Commit Changes**: Stage and commit your changes with a clear message.
4. **Add a Tag**: Add a tag for the new version.
5. **Check GitHub Pages Settings**: Whenever major changes, especially in the documentation were made, ensure that the new documentation is built and deployed after pushing your changes. (Turn 'deploy from a branch' on.)
6. **Push to Repository**: Push your commits and tags to the remote repository.
7. **Build the Package**: Use `pyproject build` to create the distribution files and verify with `twine check`.
  ```bash
    cd <path_to_your_project>
    python -m build
    twine check dist/* 
  ```
8. **Upload to PyPI**: Use `twine upload dist/*` to upload your package to PyPI.



## Local Module Testing

To install the module locally for testing, use the following command:
```bash
pip install -e .
```