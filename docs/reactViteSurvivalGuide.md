# React \+ Vite Project Survival Guide

## Creating a React project in vscode, with Vite as a local server 

*Vite allows you to run your React project in a localhost for testing.* 

1. open a terminal in vscode.  
2. cd to the __parent directory__ of where you want to add your new project folder.  
3. from the terminal: `npm create vite@latest`  
   1. then follow the prompts to __name the project dir__, the __React__ tool, the __Javascript__ language.  
4. then enter the commands they specify to go into your project folder, install the modules you need from npm, then run the demo program on your localhost. namely:  
   1.  `cd \<projectdir\>`  
   2.  `npm install`  
   3.  `npm run dev`  
      1. it will show you a localhost http address where you can see a little demo program running.  
      2. from the terminal, `control C` to exit the dev run.  
5. now is a good time to initialize and begin tracking your project repo. from the terminal in the \<projectdir\>:  
   1. `git init`  
   2. `git add .`  
6. go to GitHub, add the \<projectdir\> as a new repo. For ease of use, name the repo the same as your local projectdir).   
7. then follow GitHub's command line instructions to link the GitHub repo folder as the origin main, namely: (from your local terminal, in \<projectdir\>  
   1. `git commit \-m "first commit"`  
   2. `git branch \-M main`  
   3. `git remote add origin https://github.com/\<GitHubaccount\>/\<projectdir\>.git`  
   4. `git push \-u origin main`  
8. now in you can either replace or "husk out"  the jsx, html, and css files and replace with your own stuff. From time to time (hourly/daily) be sure to back up your code to your GitHub main branch. from your terminal in \<project dir\>   
   1. `git status *( to see what's been changed since last commit)*  
   2. `git add .   
   3. `git commit \-m "\<summary of this commit\>"   
   4. `git push  *(you don't need to specify where you are pushing since you set origin main to your github folder)*

## Deploying a React \+ Vite front-end project to GitHub Pages

9. Front-end only app? (doesn't use server-side modules like node, express, etc.)  You can deploy these to GitHub pages to allow people to access via URL.  
   1. in your project's __vite.config.js__ look for export default defineConfig({ add:   
      1. `base: "/\<projectdir\>",`  
         1. where \<gitHubfolder\> is your project's main folder, as it exists on GitHub  
   2. in your project's package.json, right below "name" key value pair add:  
      1.  `"homepage": "https://\<githubAccount\>.github.io/\<projectdir\>/",`  
   3. from the terminal, in your project folder  
      1. `npm install gh-pages \--save-dev`  
         1. installs package gh-pages, as a dev dependency (package.json will signal that you need it in dev, not production)  
   4. in your project's package.json, "scripts" section, BELOW your other scripts, add:  
      1. `"predeploy": "npm run build",`  
      2. `"deploy": "gh-pages \-d dist"`  
10. make sure you've pushed your latest code to GitHub, then in local terminal \<projectdir\>:  
    1. `npm run deploy`  
       1. this runs the predeploy then deploys everything to github pages  
11. you make another improved build? repeat `npm run deploy` as necessary to redeploy subsequent build(s).  
12. for a walkthrough, see [How To Deploy A React Vite App To Github Pages (Simple)](https://www.youtube.com/watch?v=hn1IkJk24ow)

## Deploying a full stack node/express/PostGres app with a React front end to Render.com

13. remember: GitHub Pages can't run server side packages such as node, express, axios, pg, passport, etc.  
14. So if you need server side stuff to run you'll need to deploy your site to [Render.com](http://Render.com) or another server-specializing host site, here are links on how to do it for Render.  
15. WATCH AND COMPLETE ALL 3, it's a sequence.  
    1. [How to Create a Express/Node + React Project with Vite | Node Backend + React Frontend](https://www.youtube.com/watch?v=mKmxc8TcWQ8)  
    2. [How to Bundle a React Frontend with an Express/Node Backend for Deployment](https://www.youtube.com/watch?v=1NhduUZHZEQ)  
    3. [How to Deploy a Node/Express App to Render | Node/Express Render Deployment](https://www.youtube.com/watch?v=tNpoc86cHrQ)