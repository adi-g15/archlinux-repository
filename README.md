# arch-repo

This is template repository for creating your own archlinux package repository.

## Features

- ⚙️ Works with Github Actions / Github Pages
	- You don't need to setup any server machines. This is _serverless. 😎
- ⚡ Blazingly fast
	- Build packages parallelly.
	- Use ccache to reduce compilation time.
- 🔧 Easy to setup
	- Just a few steps. See instructions below!

## How to create your own repository?

1. [Fork](https://docs.github.com/ja/github/getting-started-with-github/fork-a-repo) this repository.
2. Specify packages you want to build [here](https://github.com/kaz/arch-repo/blob/master/.github/workflows/build.yaml#L23).
3. That's all! 👏
	- Wait some minutes and visit newly-created your package repository 👉 https://github.com/[YOUR_GITHUB_ACCOUNT]/arch-repo/tree/gh-pages
