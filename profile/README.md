<div align="center">

<a href="https://planesailing.io"><img src="https://raw.githubusercontent.com/planesailingio/.github/master/profile/banner.svg" alt="Plane Sailing. Complex infra. Plain simple." width="100%"></a>

<p>
  <a href="https://planesailing.io"><img src="https://img.shields.io/badge/planesailing.io-website-2b7dbf?style=flat-square&labelColor=154560" alt="Website"></a>
  <a href="https://github.com/planesailingio/homebrew-tools"><img src="https://img.shields.io/badge/homebrew-planesailingio%2Ftools-2b7dbf?style=flat-square&labelColor=154560&logo=homebrew&logoColor=white" alt="Homebrew tap"></a>
  <a href="https://x.com/Planesailingio"><img src="https://img.shields.io/badge/follow-%40Planesailingio-2b7dbf?style=flat-square&labelColor=154560&logo=x&logoColor=white" alt="Follow on X"></a>
  <a href="https://github.com/planesailingio"><img src="https://img.shields.io/badge/licence-MIT-2b7dbf?style=flat-square&labelColor=154560" alt="MIT licence"></a>
</p>

</div>

We build developer platforms and self-service infrastructure for organisations that operate where the hyperscalers don't follow: data centres, air-gapped networks and regulated environments. Along the way we build small, sharp command-line tools for the day-to-day of platform work, and we release them here under the MIT licence.

Every tool is a single static Rust binary. No daemons, no runtime dependencies, and all of them install from one Homebrew tap.

<br>

## Featured

<table>
<tr>
<td width="50%" valign="top">

### 🎩 &nbsp;hats

<a href="https://github.com/planesailingio/hats/releases"><img src="https://img.shields.io/github/v/release/planesailingio/hats?style=flat-square&labelColor=154560&color=2b7dbf&label=release" alt="Latest release"></a>
<a href="https://github.com/planesailingio/hats/actions/workflows/ci.yml"><img src="https://img.shields.io/github/actions/workflow/status/planesailingio/hats/ci.yml?style=flat-square&labelColor=154560&label=ci" alt="CI status"></a>
<img src="https://img.shields.io/badge/macOS%20%C2%B7%20Linux-2b7dbf?style=flat-square&labelColor=154560&label=platforms" alt="macOS and Linux">

**Per-terminal identity switching and managed dotfiles.**

Wear a lot of hats? One command, `hat <name>`, switches your git identity, SSH config, cloud credentials, kube context, tokens and environment variables in the current terminal only. Think of it as chezmoi for environment variables.

- **Isolated contexts.** Each hat gets its own copy of shared tool config, and the previous hat's variables are unset on every switch, so `kubectl` or `aws sso login` in one terminal never leaks into another.
- **Dotfiles as infrastructure.** `hats plan` shows a line-level diff of your home directory. `hats apply` writes it and backs up anything it replaces.
- **An opinionated shell.** zsh, the starship prompt and curated package bundles, ready on a fresh machine in minutes.

<pre><code>brew install planesailingio/tools/hats
hats init &amp;&amp; hats plan</code></pre>

<a href="https://github.com/planesailingio/hats"><b>Repository</b></a> &nbsp;·&nbsp; <a href="https://github.com/planesailingio/hats#quick-start">Quick start</a> &nbsp;·&nbsp; <a href="https://github.com/planesailingio/hats#commands">Commands</a> &nbsp;·&nbsp; <a href="https://github.com/planesailingio/hats/releases">Releases</a>

</td>
<td width="50%" valign="top">

### 🌿 &nbsp;twig

<a href="https://github.com/planesailingio/twig/releases"><img src="https://img.shields.io/github/v/release/planesailingio/twig?style=flat-square&labelColor=154560&color=2b7dbf&label=release" alt="Latest release"></a>
<a href="https://github.com/planesailingio/twig/actions/workflows/ci.yml"><img src="https://img.shields.io/github/actions/workflow/status/planesailingio/twig/ci.yml?style=flat-square&labelColor=154560&label=ci" alt="CI status"></a>
<img src="https://img.shields.io/badge/macOS%20%C2%B7%20Linux-2b7dbf?style=flat-square&labelColor=154560&label=platforms" alt="macOS and Linux">

**A Git repository bootstrapper with predictable homes and worktrees.**

The remote URL is the path. `git@github.com:acme/widgets.git` always lands at `~/git/github.com/acme/widgets`, so there is no more hunting through `~/src`, `~/code` and `~/projects`.

- **One clone, many branches.** A bare clone is the trunk and each worktree is a twig, so `main` and `feature-x` are open side by side. No stashing, no rebuilding, no cloning the same repo twice.
- **Works with real Git hosting.** GitLab subgroups, self-hosted remotes, dry-run previews, and it never deletes or overwrites an existing repository.
- **Editor ready.** Generates a VS Code workspace for repository-wide worktree navigation. Delegates worktree management to [Grove](https://github.com/captainsafia/grove).

<pre><code>brew install planesailingio/tools/twig
twig clone git@github.com:acme/widgets.git</code></pre>

<a href="https://github.com/planesailingio/twig"><b>Repository</b></a> &nbsp;·&nbsp; <a href="https://github.com/planesailingio/twig#quick-start">Quick start</a> &nbsp;·&nbsp; <a href="https://github.com/planesailingio/twig#cli-reference">CLI reference</a> &nbsp;·&nbsp; <a href="https://github.com/planesailingio/twig/releases">Releases</a>

</td>
</tr>
</table>

<br>

## Also from the workshop

<table>
<tr>
<td width="50%" valign="top">

#### 🌱 &nbsp;[moss](https://github.com/planesailingio/moss)

<a href="https://github.com/planesailingio/moss/releases"><img src="https://img.shields.io/github/v/release/planesailingio/moss?style=flat-square&labelColor=154560&color=2b7dbf&label=release" alt="Latest release"></a>
<a href="https://github.com/planesailingio/moss/actions/workflows/ci.yml"><img src="https://img.shields.io/github/actions/workflow/status/planesailingio/moss/ci.yml?style=flat-square&labelColor=154560&label=ci" alt="CI status"></a>
<img src="https://img.shields.io/badge/macOS%20%C2%B7%20Linux%20%C2%B7%20Windows-2b7dbf?style=flat-square&labelColor=154560&label=platforms" alt="macOS, Linux and Windows">

**Cross-platform user-profile backup and restore, on top of [Kopia](https://kopia.io).**

moss discovers your profile on macOS, Linux or Windows, shows you what it would back up before it does, then restores it safely onto another machine or operating system. Kopia handles storage, encryption and deduplication. moss knows which directories make up a profile, what is a cache, what is sensitive, and where `~/Movies` becomes `~/Videos`. A 24-word recovery code is the only thing you carry between machines.

<pre><code>brew install planesailingio/tools/moss</code></pre>

</td>
<td width="50%" valign="top">

#### 🐦 &nbsp;[gannet](https://github.com/planesailingio/gannet)

<a href="https://github.com/planesailingio/gannet/releases"><img src="https://img.shields.io/github/v/release/planesailingio/gannet?style=flat-square&labelColor=154560&color=2b7dbf&label=release" alt="Latest release"></a>
<a href="https://github.com/planesailingio/gannet/actions/workflows/ci.yml"><img src="https://img.shields.io/github/actions/workflow/status/planesailingio/gannet/ci.yml?style=flat-square&labelColor=154560&label=ci" alt="CI status"></a>
<img src="https://img.shields.io/badge/macOS%20%C2%B7%20Linux%20%C2%B7%20Windows-2b7dbf?style=flat-square&labelColor=154560&label=platforms" alt="macOS, Linux and Windows">

**Install CLI tools straight from GitHub releases, with instant rollback.**

`gannet install sharkdp/fd` asks GitHub for the latest release, scores every asset against your OS and architecture, and puts the right binary on your PATH. It keeps the previous version on disk, so `gannet rollback` is a symlink swap that works offline. No daemon, no config file, and if it has a GitHub release you can install it. Named after the seabird: they dive, they grab, they rarely miss.

<pre><code>brew install planesailingio/tools/gannet</code></pre>

</td>
</tr>
</table>

<br>

## Installing

All four tools ship from the [planesailingio/tools](https://github.com/planesailingio/homebrew-tools) Homebrew tap on macOS and Linux, and as prebuilt archives on each project's releases page. The tap also carries Grove, the worktree tool twig builds on.

```sh
brew install planesailingio/tools/hats
brew install planesailingio/tools/twig
brew install planesailingio/tools/moss
brew install planesailingio/tools/gannet
```

hats also has a one-line installer that sets up Homebrew if you don't have it yet, then installs hats. It does not touch your home directory until you run `hats apply`.

```sh
curl -fsSL https://planesailingio.github.io/hats/install.sh | sh
```

Prefer building from source? Each repository is a standard Cargo project: clone it and run `cargo install --path .`.

<br>

## About Plane Sailing

We are a DevSecOps and platform engineering consultancy based in London. We help organisations in regulated industries run developer platforms, data pipelines and self-service infrastructure on their own hardware, with open source first and no vendor licensing fees. The tools above are the ones we reach for every day, shared in the hope they save you the same time they save us.

Issues and pull requests are welcome on every repository.

<div align="center">
<br>
<a href="https://planesailing.io">planesailing.io</a> &nbsp;·&nbsp;
<a href="https://x.com/Planesailingio">@Planesailingio</a> &nbsp;·&nbsp;
<a href="https://github.com/planesailingio/homebrew-tools">Homebrew tap</a>
<br><br>
<sub>Plane Sailing · London, England</sub>
</div>
