# Git - Best practices

## Feature branches
Every story should have a corresponding feature branch with naming convention 'features/PRES-XX'. 
Always use rebase instead of merge.Feature


## Correct rebase
Example below is to merge your changes on feature branch 'features/PRES-XX' to master. However same procedure should be followed if you want to merge local branch to a feature branch.

  1. You should have no pending changes in the git folder. In case you have, they should be committed or stashed before you continue.
  2. Make sure you have the latest code on your feature branch
    {% highlight bash %}git pull --rebase origin features/PRES-XX{% endhighlight %}
  3. Go to master branch
    {% highlight bash %}git checkout master{% endhighlight %}
  4. Make sure you have the latest version of the master branch.
    {% highlight bash %}git pull --rebase origin/master{% endhighlight %}
  5. Go to the feature branch
    {% highlight bash %}git checkout features/PRES-XX{% endhighlight %}
  6. Optional: Squach your commits before going further, this can be done to cleanup the git history before it's added to the master branch. The number behind HEAD~ is used to determine how many commits will be shown in the interactive rebase.
    {% highlight bash %}git rebase -i HEAD~3{% endhighlight %}
  7. Rebase the feature branch with master
    {% highlight bash %}git rebase master{% endhighlight %}
  8. In case there are conflicts due to the rebase they must be resolved. Once they are solved you can continue your rebase
    {% highlight bash %}
    git add .
    git rebase --continue
    {% endhighlight %}
  9. Make sure that during this process there hasn't been a commit on master branch. In case there was you will need to redo the steps from step 3.
  10. You are ready to push the changes to your feature branch
    {% highlight bash %}git push -f origin features/PRES-XX{% endhighlight %}

After this commit a pull request can be created in github.