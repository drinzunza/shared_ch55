Git for Pairs

🎯 Learning Goals
	•	Understand the flow of Git + GitHub collaboration
	•	Learn how two developers can work from the same repository
	•	Practice resolving merge conflicts

⸻

📚 Vocabulary!
	•	Merge Conflict – Conflicting changes on the same line or file
	•	Pull Request (PR) – Propose merging one branch into another
	•	Clone – Download a remote repo to your local machine
	•	Fork – Make your own copy of a GitHub repo

⸻

🔁 Warm-Up: Git Commands Review

Creating a Local Repository

git init

Saving Changes

git status
git add file_name.html
git commit -m "Add message"

Creating and Switching Branches

git checkout -b branch_name
# OR
git branch branch_name
git checkout branch_name

Interacting with Remote

git pull origin branch_name
git push origin branch_name
git remote -v
git remote add origin <remote-URL>


⸻

🔄 Clone vs. Fork + Clone
	•	Clone: You are working with the same repo. Ideal for teams or pair programming.

git clone git@github.com:username/repo-name.git


	•	Fork + Clone: You need to copy someone else’s repo when you don’t have write access.

⸻

⚔️ Merge Conflicts

When Git can’t automatically decide which changes to keep, it creates a merge conflict.

Example conflict:

<<<<<<< branch_name
<h1>Welcome from Person A</h1>
=======
<h1>Welcome from Person B</h1>
>>>>>>> main

To resolve:
	•	Choose the correct code
	•	Delete the conflict markers
	•	Save, stage, and commit

Use the GitHub conflict resolution tool or your editor.

⸻

👥 Git Flow for Pairs

👤 Person A
	1.	Create a folder and cd into it
	2.	Initialize Git

git init

	3.	Create repo on GitHub
	4.	Connect local to GitHub

git remote add origin git@github.com:username/repo-name.git

	5.	Create file:

touch index.html

	6.	Add initial code to index.html (e.g., <h1>Hello!</h1>)
	7.	Stage and commit:

git add index.html
git commit -m "Initial commit"
git push origin main

	8.	Add Person B as collaborator
	9.	Create a feature branch and modify index.html

git checkout -b new_feature
# Edit file (change heading, etc.)
git add index.html
git commit -m "Update heading text"
git push origin new_feature

👤 Person B
	1.	Accept invite
	2.	Clone repo:

git clone git@github.com:username/repo-name.git
cd repo-name

	3.	Create new branch and edit index.html

git checkout -b add_content
# Edit heading differently than Person A
git add index.html
git commit -m "Alter heading text"
git push origin add_content

	4.	Open a Pull Request for add_content

👤 Person A
	1.	Review PR from Person B
	2.	Approve and merge it
	3.	On new_feature branch, sync with updated main

git pull origin main

	4.	Resolve any merge conflicts
	5.	Commit and push the resolved file
	6.	Open a PR for new_feature

👤 Person B
	1.	Review and merge Person A’s PR

🔄 Both

git checkout main
git pull origin main


⸻

✅ Checks for Understanding
	•	What’s the Git flow for pair programming?
	•	What’s a merge conflict? How do you resolve it?

⸻

📎 Additional Resources
	•	Git - the Simple Guide
	•	Pro Git Book

⸻

Happy Pairing! 🤝💻