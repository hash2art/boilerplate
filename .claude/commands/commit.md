---
Description: Create a commit in the Conventional Commits style
allowed-tools: Bash(git *)
---
1. Run `git add .`
2. Analyze `git diff --cached`
3. Generate a message according to the Conventional Commits specification (feat, fix, etc.)
4. Run `git commit -m "<message>"`
