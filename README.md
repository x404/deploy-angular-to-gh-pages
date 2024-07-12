# Deploying an Angular App to Github pages


1. Preconditions:
1.1 A github account
1.2 A Github Repo

2. Deployment to gh-pages:
2.1 Create a Github repository for your project.
2.2 Push your code to the main branch
2.3 Create a **gh-pages** branch - This is an invaluable hack that will help us get the gh-pages link to help us set the base-href
Navigate to the settings of your Github repo to get the link to the published site

3. Back to your project locally add the [angular-cli-ghpages](https://www.npmjs.com/package/angular-cli-ghpages)
```
ng add angular-cli-ghpages
```


4. Deploy your app using **ng deploy** command
```
ng deploy --base-href=your-link-to-gh-pages
```
Ex.
```
ng deploy --base-href=https://x404.github.io/deploy-angular-to-gh-pages/
```

Note: 
- replace your link to gh-pages with your actual link to gh-pages

5. Copy all files from dist directory to docs directory or before deploy your app with **ng deploy** change the output path you have to change **outputPath** and the build options.


UPDATED: If the App shows the README file, please navigate to the gh-pages setting on Github and ensure that the selected branch is gh-pages but not main or master.


References:
https://www.npmjs.com/package/angular-cli-ghpages
https://angular.io/guide/deployment#deploy-to-github-pages 
npmjs package 'angular-cli-ghpages' 
