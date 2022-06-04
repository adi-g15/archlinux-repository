# ArchLinux Repository

This is an **automated** ArchLinux package repository.
You can easily add any AUR packages you want.

This was forked from [kaz's repository](https://github.com/kaz/archlinux-repository-boilerplate). Major changes I made are:

1. Use all cores available
2. Uploads only the final built package, instead of complete build tree [(now upstream too 😁)](https://github.com/kaz/archlinux-repository-boilerplate/pull/6)
3. GitHub Actions runs daily build but the commiter will NOT be you (upstream it's on your behalf)

## Features

- ⚙️ Works with GitHub Actions / GitHub Pages
	- You don't need to setup any server machines. This is _serverless_. 😎
- ⚡ Blazingly fast
	- Build packages parallelly.
	- Use ccache to reduce compilation time.
- 🔧 Easy to setup
	- Just a few steps. See instructions below!

## How to create your own repository?

You can go to original repository or fork the current one :D

1. You can fork this repository, or use the original repository as template 
	- You can find detailed instruction [HERE](https://docs.github.com/en/free-pro-team@latest/github/creating-cloning-and-archiving-repositories/creating-a-repository-from-a-template), or [fork](https://docs.github.com/en/free-pro-team@latest/github/getting-started-with-github/fork-a-repo) this repository.
	- Original repository is [HERE](https://github.com/kaz/archlinux-repository-boilerplate).
2. Specify packages you want to build [HERE](./.github/workflows/build.yaml#L27-L31). ✍
3. [Enable GitHub Pages](https://docs.github.com/en/free-pro-team@latest/github/working-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site) and select `gh-pages` branch as a publishing source.
	- Due to limitation of `GITHUB_TOKEN`, GitHub Actions cannot make GitHub Pages enable in workflow. So you have to activate it manually. 😥
4. That's all! 👏
	- Wait some minutes and visit newly-created your package repository 👉 `https://{{your_account}}.github.io/{{your_repository_name}}/`

## Tips

- Edit [.github/workflows/build.yaml](./.github/workflows/build.yaml) to modify build behavior.
