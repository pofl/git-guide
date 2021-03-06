# Mastering Git

- [Tags](https://blog.daftcode.pl/how-to-become-a-master-of-git-tags-b70fbd9609d9)

- `git add --patch`

- `rebase` with `-p` and `-r`
    - `-r` / `--rebase-merges` <https://git-scm.com/docs/git-rebase#_rebasing_merges>
    - `-p` / `--preserve-merges` <https://stackoverflow.com/questions/4783599/rebasing-a-git-merge-commit>

- [Untracking files after adding them to .gitignore](https://eric.blog/2014/05/11/remove-files-from-git-addingupdating-gitignore/)
    - `git rm --cached <file>` for single files
    - for many files/directories

          git rm -r --cached .
          git add -A
          git commit -am 'Removing ignored files'

- `checkout -m`

- `git branch -f master HEAD~3` is equivalent to  

      git checkout master
      git reset --hard HEAD@{1}~3


- [Set branch to current ref](https://stackoverflow.com/questions/7580542/git-set-branch-to-current-ref) (`git checkout -B <branch>`)

- Comparison of `git add .`, `git add --all` (-A) and `git add --update` (-u): <https://stackoverflow.com/a/26039014/9039623>

- If you like to use Emojis in commit messages please follow this guideline which tries to standardise the semantics of Emojis: <https://gitmoji.carloscuesta.me/>

- How Git works internally
    - [Git commits are not stored as diffs](https://medium.com/@gohberg/the-biggest-misconception-about-git-b2f87d97ed52)
    - <https://smusamashah.github.io/blog/2017/10/14/explain-git-in-simple-words>
    - [Git Internals by Scott Chacon](https://github.com/pluralsight/git-internals-pdf) (how git works internally)

- diff
    - word-diff
    - dir-diff
    
- Cherry-picking vs Merging
    - [Stop cherry-picking, start merging](https://devblogs.microsoft.com/oldnewthing/?p=98325)
    - [Stop merging if you need to cherry-pick](https://devblogs.microsoft.com/oldnewthing/?p=99195)
        - Is the last post in the series "Stop cherry-picking, start merging" and a response to the original articles from another team at Microsoft.
        - "the problem case is where you cherry-pick between two branches that will eventually merge. If the two branches never merge, then there's no need to get all fancy with your cherry-picking."
    
- subtree
    - <https://tsh.io/blog/git-subtree-or-how-i-stopped-worrying-and-learned-to-love-external-dependencies/>
    - <https://medium.com/@porteneuve/mastering-git-subtrees-943d29a798ec>
    - <https://www.atlassian.com/git/tutorials/git-subtree>

- Patches in Git
    - The output `diff` produces is the format of the Unix program 'patch' (<https://stackoverflow.com/a/8279783/9039623>)
    - The Linux kernel uses a strange workflow around sending such patches/diffs via e-mails to other maintainers. (<https://git-scm.com/book/id/v2/Distributed-Git-Maintaining-a-Project>)

- blame and `git log --follow -- filename`
    - <https://stackoverflow.com/questions/3701404/list-all-commits-for-a-specific-file>

- Configuration
    - git log
        https://stackoverflow.com/questions/1057564/pretty-git-branch-graphs/35075021
    - Aliases
    - [How to keep git log and less output on the screen](http://serebrov.github.io/html/2014-01-04-git-log-and-less-keep-output.html)

- Clearing up the confusion about 'LOCAL' and 'REMOTE' during merges/rebases: https://stackoverflow.com/questions/3051461/git-rebase-keeping-track-of-local-and-remote

- Git hooks
    - https://rock-it.pl/automatic-code-quality-checks-with-git-hooks/

- Tools
    - difftool, mergetool
        - <https://developer.atlassian.com/blog/2015/12/tips-tools-to-solve-git-conflicts/>
    - tig
        - <https://www.atlassian.com/blog/git/git-tig>
    - lazygit
        - <https://github.com/jesseduffield/lazygit>

- `reflog`

- bisect

- rerere

- <https://stackoverflow.com/questions/4044368/what-does-tree-ish-mean-in-git>

- [6 Git Aha Moments](https://henrikwarne.com/2018/06/25/6-git-aha-moments/)
