# Hugo-PaperMod-NetlifyCMS-Starter

This repository should help you get started with using Hugo and the Papermod theme quickly on Netlify with NetlifyCMS.  It's based on the [hugo-Papermod example site](https://github.com/adityatelange/hugo-PaperMod), with NetlifyCMS support added in the /static/admin directory.  

## Install

Here's the quickest way to get started. Some of the steps below may vary depending on your setup, but this is more or less what I did when setting this up:

1. Use the deploy to Netlify button below. This will clone this repository into your Github account, and setup continuous integration/deployment through your Netlify account:

[![Deploy to Netlify](https://www.netlify.com/img/deploy/button.svg)](https://app.netlify.com/start/deploy?repository=https://github.com/cjreinhardt/Hugo-PaperMod-NetlifyCMS-Starter)

2. Open a terminal or command prompt and clone your newly created repository onto your local machine
```
git clone https://github.com/YourUsername/YourNewRepositoryname.git
```
3. If you don't already have Hugo installed, now's the time to make that happen!  Read the [Hugo install docs here](https://gohugo.io/getting-started/installing/).

4. Once Hugo is installed go to your repository directory on your local machine.  Edit congif.yml in the root directory.  Here you can change alot of the content displayed by Papermod (like the text on the homepage), and also adjust a ton of options.  Check out the  [Papermod docs here for more info](https://github.com/adityatelange/hugo-PaperMod/wiki/Features)).  

5. When you're done editing start Hugo with this command:
```
hugo server -D
```

6. You should now be able to see your site! Hugo will let you know where you can view your site in the terminal (it's usually at localhost:1313)

7. If you want, you can run NetlifyCMS locally to edit or add posts (insytead of editing the .md files directly).  Uncomment this line in /static/admin.config.yml:
```
local_backend: true
```

8. If you don't have Node installed, you'll need to install it, [see their docs here](https://nodejs.org/en/download/).  

9. Open a new terminal, go to your repository directory and run this command to start NetlifyCMS locally (note that this is a beta feature, see Netlify's [docs on this here](https://www.netlifycms.org/docs/beta-features/)):
```
npx netlify-cms-proxy-server
```

10. If everything has worked you should be able to edit posts in NetlifyCMS by going to /admin. Each post has options for most of Papermod's post variables, 
[read more about them here](https://adityatelange.github.io/hugo-PaperMod/posts/papermod/papermod-variables/).  

11. Once you've got your site all setup and posts edited make sure to comment out line 4 of /static/admin.config.yml before you push your changes back to github:
```
#local_backend: true
```

12. When you're ready you'll want to add/stage all your changes, commit your changes to your local repository, then push your changes back to your Github repository. You may need to setup a [personal access token](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/creating-a-personal-access-token) or [ssh key](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/adding-a-new-ssh-key-to-your-github-account).  Once you push your changes to Github, Netlify will see that you've updated your repository and push all your changes to your public site. Voila! :tada:
```
git add -A
git commit -m "Add a useful commit message"
git push origin main
```

## More Info on Hugo Papermod

Visit the Hugo Papermod Github repo => [hugo-Papermod at Github](https://github.com/adityatelange/hugo-PaperMod)

Read the Hugo Papermod Wiki => [hugo-PaperMod - Installation](https://github.com/adityatelange/hugo-PaperMod/wiki/Installation)

Find out more about Hugo here => [https://gohugo.io](https://gohugo.io)
