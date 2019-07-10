# Gitflow

Set of helpful guidelines and MATE conventions when using `gitflow`.

- Gitflow feature should be used when you want to start working on a additional feature
- Gitflow release should be used when you finished a new feature and want to merge it with the production branch
- Gitflow hotfix should be used when you have to do a quick error correction on the production branch

## Gitflow feature

**To use in develop branch when you are starting working on a new feature**

```
git flow feature start mv_IE10_banner
git status
git add .
git commit -m"remove console.log”
git push
```

### Now create a pull request in bitbucket

![Screenshot 2019-07-10 at 12 59 01](https://user-images.githubusercontent.com/52755209/60988330-aea9a300-a343-11e9-8463-c2770bd176d5.png)

- from feature to develop branch
- add title
- add reviewers
- create pull request

After the pull request is approved by reviewers, in terminal, finish the feature and push to master. Use your initials as a part of feature naming convention.

```
git flow feature finish 'mv_IE10_banner’
git branch
git push
```

## Gitflow release

```
git flow release start 1.0.2`
git status
git add .
git commit -m"feature description”
git flow release finish '1.0.2’
git branch
git push
git checkout master
git push
git push —tags
```

### Gitflow hotfix

```
git flow hotfix start 1.0.0.hotfix4
git status
git add .
git commit -m"remove console.log”
git flow hotfix finish '1.0.0.hotfix4’
git branch
git push
git checkout master
git push
git push —tags
```

Additional links:

- [Gitflow Cheatsheet](https://danielkummer.github.io/git-flow-cheatsheet/) for more information.
- [Gitflow Official Website](https://www.atlassian.com/git/tutorials/comparing-workflows/gitflow-workflow)
