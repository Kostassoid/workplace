Git commit hook
===============

Requires JIRA issue id in commit message.

Installation
------------

Create and enable template for every new git repo:

```shell
mkdir -p ~/.git-templates/hooks
curl https://raw.githubusercontent.com/kostassoid/workplace/master/git/hooks/commit-msg >~/.git-templates/hooks/commit-msg
chmod a+x ~/.git-templates/hooks/commit-msg
git config --global init.templatedir '~/.git-templates'
```

Install for existing repo:
```shell
git init
```

Install for existing repo with submodules:
```shell
git submodule foreach git init
```

Skipping verification for single commit:
```shell
git commit --no-verify -m "..."
```
