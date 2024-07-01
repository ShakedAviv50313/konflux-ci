Contributing Guidelines
===

<!-- toc -->

- [Editing Markdown Files](#editing-markdown-files)
- [Using Kubelinter](#using-Kubelinte)

<!-- tocstop -->

# Editing Markdown Files

If the structure of markdown files containing table of contents changes, those
need to be updated as well.

To do that, run the command below and add the produced changes to your PR.

```bash
find . -name "*.md" | while read -r file; do
    npx markdown-toc $file -i
done
```


# Using Kubeliter

Please consider using [Kubelinter](https://docs.kubelinter.io/#/) locally before submitting a PR to this repository.
Konflux-ci's CI tests consist of Kubelinter, and it will fail the tests for PRs which are not passing Kubelinter's check.
