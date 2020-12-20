# active-forks

> Find the active github forks of a project

This project allows you to find the most active forks of a repository.

I added a couple of features useful to compare forks:
* works after providing a **personal GitHub token**. It is used only to increase the limits to query to API. The token is stored in Local Storage only, not sent anywhere except for the GitHub API. If the token is not stored in Local Storage, it can be provided via URL query string parameter ```authToken```.
* include the **original repository** in the list, marked in bold
* after expanding **Options**, it is possible to increase the **maximum amount of forks** to retrieve and to utilize some kind of caching
* retrieve **commits of each fork** and show the differences
* click on box in the **Diff** column to see the commits

## Optimizations

Because this version retrieves commits from every fork which is slow and uses your quota (it resets every hour, don't worry), I added two options for caching results:
* **Same size** - if a fork has the same size as a fork that has already been read, it is assumed to be the same and contain the same commits.
* **Same Push Date** - same but looks at the Last Push date.
If both are selected, both conditions have to be satisfied at the same time.
If the condition is satisfied, commits for the second fork are not retrieved but assumed to be the same as in the first fork.


[Find Active Fork](https://lukasznojek.com/projects/active-github-forks/)

![Screenshot](screenshot.png "Active Forks in Action")
