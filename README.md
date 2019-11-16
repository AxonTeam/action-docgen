# action-docgen

Action to generate docs on a repo and commit the changes automatically.  

This ation was inspired from [discordjs](https://github.com/discordjs/action-docs/).  

This action will generate doc in the repo based of the docgen npm script that need to exist in the package.json.  
It will then commit these changes in the same branch.  
This action targets user with a docs/ folder withing their current branch.  
