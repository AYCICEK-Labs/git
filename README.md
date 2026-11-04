# git

The Git standards of AYÇİÇEK Labs: line endings, binary files and ignored files.

| File                       | Purpose                                                                                                     |
| -------------------------- | ----------------------------------------------------------------------------------------------------------- |
| `.gitattributes`           | The standard itself: LF everywhere, CRLF only for Windows scripts, binary files, generated files collapsed. |
| `gitignore/Base.gitignore` | Every repository: OS and editor files, environment files and keys, Claude Code's personal settings, logs.   |
| `gitignore/Node.gitignore` | Node projects: `node_modules`, build output, coverage.                                                      |
| `gitignore/Rust.gitignore` | Rust projects: the `target` build folder.                                                                   |

A project's `.gitignore` is `Base` followed by the templates of its stacks.

## Use it in a project

```sh
base=https://raw.githubusercontent.com/AYCICEK-Labs/git/main
curl -fsSL "$base/.gitattributes" -o .gitattributes
{ curl -fsSL "$base/gitignore/Base.gitignore"; echo; curl -fsSL "$base/gitignore/Node.gitignore"; } > .gitignore
```

## License

[MIT](LICENSE) © Yunus Emre AYÇİÇEK
