*Indigo*, is a Python formatter, forked from
*[Pyink](https://github.com/google/pyink)* (itself forked from [Black](https://github.com/psf/black) with a few different formatting
behaviors. I intend to keep rebasing on top of *Pyink*'s latest changes.

# What are the main differences?

*   

# How do I use *Indigo*?

Same as `pyink`, except you'll use `indigo`. All `black` and `pyink` command line options are
supported by `indigo`. To configure the options in the `pyproject.toml` file, you
need to put them in the `[tool.indigo]` section instead of `[tool.pyink]` or `[tool.black]`.

## Is there a VS Code extension for *Indigo*?

No, but with a bit workaround, you can use the
[Black Formatter](https://marketplace.visualstudio.com/items?itemName=ms-python.black-formatter)
extension. After installing *Indigo* and the extension, you can set these in VS
Code's `settings.json`:

```json
{
    "[python]": {
        "editor.defaultFormatter": "ms-python.black-formatter"
    },
    "black-formatter.path": [
        "path/to/indigo"
    ]
}
```

## Can I use *Indigo* with the [pre-commit](https://pre-commit.com/) framework?

Yes! You can put the following in your `.pre-commit-config.yaml` file:

```yaml
repos:
  - repo: https://github.com/angus-lherrou/indigo
    rev: 23.3.0
    hooks:
      - id: indigo
        # It is recommended to specify the latest version of Python
        # supported by your project here, or alternatively use
        # pre-commit's default_language_version, see
        # https://pre-commit.com/#top_level-default_language_version
        language_version: python3.9
```

# Why the name?

Indigo is my favorite color, and I don't care about character counts.

# License

[MIT](./LICENSE)

# Contributing

Don't.
