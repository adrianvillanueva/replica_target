# How to Mirror a Git Repository 

1. Clone the repo you want to mirror.
   ```
   git clone --mirror <source_repo_url> source_replica
   ```
2. Add the destination remote repo. Give it a meaningful nickname like "sync."
   ```
   cd source_replica
   git remote add sync <destination_repo_url>
   ```
3. Pull down changes from the source repo and push them to the destination repo.
   ```
   git remote update
   git push sync --mirror
   ```
