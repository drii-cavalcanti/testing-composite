1) Let's suppose you remotely pushed your my_env.txt file. A colleague asks you to remove this information from Git. What's your colleague worried about?
Colleague is most likey concerned with with sensitive informaiton being shared on the repo

2) If you modify the file in your workspace, then push it, will it be enough? (It's not). Why?
It will not, because the changes will be on the repo but can be restored on the histroy 

3) If you delete the file and push it, then create a new one with the rest of the information, is it enough? (It's not). Why?
It will not, because it will add the new commit to the repo but on the history it will still show

4) How to fix this? How do you remove something from Git history?
Personally, I'd use git rebase -i to rewrite the history / commit

5) Which commands would you use? What are the consequences for other developers?
I'd use git rebase -i HEAD~2,
Consequences for the other Dev's is that the history will be rewritten completely, you'd need to think twice before doing a rebase on a repo that other devs are working on.
