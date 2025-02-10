# GitCommands

## Diagram of a standard git-flow merge to main with deployment

![gitflow (1)](https://github.com/user-attachments/assets/f332c224-99a5-4367-9a15-7549a88ba7a5)


## Steps and Git CLI Commands:

### 1. Create a Feature Branch:
- git checkout develop
- git checkout -b feature/my-feature

### 2. Work on the Feature:
- git add .
- git commit -m "Add new feature"
- git push origin feature/my-feature

### 3. Merge Feature into `develop`
- git checkout develop
- git merge feature/my-feature
- git push origin develop
 
### 4. Merge `develop` into `main`:
- git checkout main
- git merge develop
- git push origin main

### 5. Tag the Release:
- git tag v1.0.0
- git push origin v1.0.0
  

### 6. Deploy to Production:
- Deploy the `main` branch to production (this step depends on your deployment process).
./deploy.sh
