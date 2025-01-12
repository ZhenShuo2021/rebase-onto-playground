# 練習 git rebase onto 的範例

[English Readme](#example-for-practicing-git-rebase-onto)

網路上所有介紹 git rebase --onto 的文章都只講了一半，你們知道排列組合之後他總共有多少種用法嗎？總共有 6 種！！！

1. git rebase --onto x  
2. git rebase --onto x y  
3. git rebase --onto x y z  
4. git rebase x --onto y  
5. git rebase x --onto y z  
6. git rebase x y --onto z  

更不要說在不同分支進行 rebase 結果還會不一樣，如果看不懂文檔就直接使用 rebase onto 功能是非常危險的，因此我寫了一篇文章介紹[如何讀懂文檔並且介紹 rebase onto 用法](https://docs.zsl0621.cc/docs/git/rebase-onto)，這個 repo 則是讓大家在 rebase 前可以先測試結果的模版，以免發生預期之外的結果。

這個 repo 和別的 repo 的差別簡單精煉，沒有多餘的檔案，提交訊息簡短並且歷史和[官方文檔](https://git-scm.com/docs/git-rebase)的基本一樣，所以可以很輕鬆的對照。repo 總共有三個分支：

1. main: 新增了 a1/a2/a3/b1/b2/b3 檔案
2. feat: 在 a1/a2/a3 分別修改一行並標注修改來自 feat branch
3. fix: 同上，標注修改來自 fix branch

如此一來你就可以很快的定位到現在的分支和 rebase 來源是哪裡。

---

# Example for Practicing Git Rebase Onto

Most articles online about git rebase --onto only explain half of the story. Do you know how many possible combinations there are after you consider all scenarios? There are **six** in total!  

1. git rebase --onto x  
2. git rebase --onto x y  
3. git rebase --onto x y z  
4. git rebase x --onto y  
5. git rebase x --onto y z  
6. git rebase x y --onto z  

And it gets even more confusing when you rebase across different branches, as the results may vary. Using the rebase onto functionality without fully understanding the documentation can be extremely risky. That’s why I wrote an article explaining [how to read the documentation and understand the usage of rebase onto](https://docs.zsl0621.cc/docs/git/rebase-onto). This repo serves as a template that allows you to test the results before performing a rebase, helping you avoid unexpected outcomes.

This repo stands out for its simplicity and conciseness. It has no extra files, short commit messages, and a commit history that closely matches the [official documentation](https://git-scm.com/docs/git-rebase), making it easy to compare results. The repo contains three branches:

1. **main**: Adds files `a1`, `a2`, `a3`, `b1`, `b2`, and `b3`.  
2. **feat**: Modifies one line in each of `a1`, `a2`, and `a3` with comments indicating that the changes come from the feat branch.  
3. **fix**: Does the same as feat, but marks changes as coming from the fix branch.  

With this setup, you can quickly identify your current branch and the rebase source, making it easier to predict the outcome of your rebase operation.  
