# Deploy Codebase to Github

- First, create a public repository on your personal github page.

- Remove the sdaml origin from your local git repository, 
```bash
git remote rm origin
```

- Add your newly created repository as a remote origin and push the code to github
```bash
 git status
 git add .
 git commit -m "added Tachyons"
 git remote add origin <your-repo-URL>
 git push -u origin master
```

