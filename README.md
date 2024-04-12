# zed-twig

Extension to enable syntax highlighting for Twig files in Zed.

## Formatting

Unfortunately, the extension does not support formatting. The available Prettier plugins didn't worked well, so I've decided to skip this. If you want to format your Twig files, install [https://www.djlint.com/docs/getting-started/](djLint) and configure Zed/your project like this:

```json
{
  "language_overrides": {
    "Twig": {
      "format_on_save": {
        "external": {
          "command": "bash",
          "arguments": [
            "-c",
            "cat {buffer_path} | djlint - --profile=nunjucks --reformat"
          ]
        }
      }
    }
  }
}
```
