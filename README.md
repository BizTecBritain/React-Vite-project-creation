# React Vite project creation
1. Install Node.js with all dependencies
2. Open react folder in cmd (ADMIN)
3. Run the following
    ```
    $ npm create vite@latest
    ```
4. Add project name
5. Select the correct items
    ```
    REACT
    Javascript or Typescript
    ```
6. Enter project name directory and run commands
    ```
    $ cd project-name
    $ npm install
    $ npm run dev
    ```
7. Open folder in VS Code and edit and see live updates
8. Create blank Github repo DO NOT CHECK ANY BOXES TO ADD LICENSE, GITIGNORE OR README
9. Git bash in project directory and run the following
    ```
    $ git init
    $ git add .
    $ git commit -m "First Commit"
    $ git branch -M main
    $ git remote add origin http://github.com/username/repo-name.git
    ```
10. Push to github from Github desktop
11. Edit ```vite.config.js``` file
    ```
    import { defineConfig } from 'vite';
    import react from '@vitejs/plugin-react';
    
    // https://vitejs.dev/config
    export default defineConfig({
      base: "/repo-name/",
      plugins: [react()]
    })
    ```
12. Edit ```package.json```
    * Add homepage to dict under version line
        ```
        "homepage": "https://username.github.io/repo-name",
        ```
    * Add deploy scripts under scripts dictionary
        ```
        "predeploy": "npm run build && git add dist -f && git commit -m \"Adding dist\"",
        "deploy": "git subtree push --prefix dist origin gh-pages",
        ```
13. To deploy run the following in Git bash
    ```
    npm run deploy
    ```
14. In the Github Repo under Settings -> Pages set the deploy branch to gh-pages
15. Wait a couple of minutes for the Github repo to update and it will work
