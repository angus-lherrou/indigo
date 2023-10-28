*Nila*, is a Python formatter, forked from
*[Pyink](https://github.com/google/pyink)* (itself forked from [Black](https://github.com/psf/black) with a few different formatting
behaviors. I intend to keep rebasing on top of *Pyink*'s latest changes.

# What are the main differences?

*   

# How do I use *Nila*?

Same as `pyink`, except you'll use `nila`. All `black` and `pyink` command line options are
supported by `nila`. To configure the options in the `pyproject.toml` file, you
need to put them in the `[tool.nila]` section instead of `[tool.pyink]` or `[tool.black]`.

## Is there a VS Code extension for *Nila*?

No, but with a bit workaround, you can use the
[Black Formatter](https://marketplace.visualstudio.com/items?itemName=ms-python.black-formatter)
extension. After installing *Nila* and the extension, you can set these in VS
Code's `settings.json`:

```json
{
    "[python]": {
        "editor.defaultFormatter": "ms-python.black-formatter"
    },
    "black-formatter.path": [
        "path/to/nila"
    ]
}
```

## Can I use *Nila* with the [pre-commit](https://pre-commit.com/) framework?

Yes! You can put the following in your `.pre-commit-config.yaml` file:

```yaml
repos:
  - repo: https://github.com/angus-lherrou/nila
    rev: 23.3.0
    hooks:
      - id: nila
        # It is recommended to specify the latest version of Python
        # supported by your project here, or alternatively use
        # pre-commit's default_language_version, see
        # https://pre-commit.com/#top_level-default_language_version
        language_version: python3.9
```

# Why the name?

Nila comes from the Sanskrit word नील _nīla_, which was borrowed through Persian 
into Arabic as the word for the color indigo. Indigo is my favorite color. I also
have a friend named Nila who gave her permission to have this project named after
her.

# License

[MIT](./LICENSE)

# Contributing

Don't.
