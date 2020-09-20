# Purpose 
This folder is the template folder for github repositories. Use this as a base to create and commit code to github.com 

# 1. Create the new folder

Copy the entire contents of the ```docker-template``` folder and re-name the ```my-new-folder-2```

# 2. Initialise git 

- Navigate to ```my-new-folder-2``` folder in the terminal
```bash
ssh-add
git init
git add .
git status 
git commit -m "Init new repo first commit" 
```

# 3. Create a new repo at github.com 

- Create a repository at github.com with the same name as the new folder ```my-new-folder-2```
- Select public or private as desired
>Use this option __…or push an existing repository from the command line__
```
git remote add origin git@github.com:CrazyDaffodils/my-new-folder-2.git
git push -u origin master
```

# 4. Update required packages 
- Navigate to ```my-new-folder-2``` folder in the terminal and to open the folder in VS Code
```bash
code . 
```
- Modify the ```docker/Dockerfile``` with the appropriate packages. Then rebuild docker images
```bash
docker-compose up --build
```
- Push the changes to git & github.com
```bash
git add .
git status
git commit -m "Package changes"
git push
```