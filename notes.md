# Create a branch
- 99% you need to be in main
- pull the latest from main
- git checkout -b <name>

# Change branches
git checkout <name>


# List local branhces
git branch
use Q to quit


# Create a commit
git add -A
git commit -m "ANY MESSAGE HERE"

# Push a branch
git push 
(will give you an error, and the full command to copy and paste)


# Check your branch
- git status
- left bottom corner on VS code



# Recommendations

## After merge
- Once your PR is merged
- go back to main branch
- pull the latest origin->main
- create a new branch for new functionality





# Steps fo fix Merge Issues/Conflicts

- Go back to main
- pull
- Go back to your feature branch
- git merge main
- You will get the issues
- fix them
- commit and push


