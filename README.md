# Hugo Blog

Hugo is a static website generator in Markdown. It's very easy to get started, it has hundreds of free template available and your can publish your static website for free on Github!


## Dependencies

Hugo must be installed! Please refer to this page for more information:

https://gohugo.io/


1. For MacOS:

        brew install hugo

2. For Windows:

        choco install hugo -confirm

3. For linux:

        snap install hugo


## Getting started

1. Clone this repository with recursion for submodules

        git clone https://github.com/antoniofagardo/hugo-blog.git --recurse-submodules && cd hugo-blog

2. Brownse the themes available and choose one that you like

    https://themes.gohugo.io/

3. Let's add this new theme to our repo as a submodule as we want to stay up-to-date

        git submodule add https://github.com/nirocfz/arabica themes/arabica

4. Add a new post! It's simple and easy:

        hugo new post/my-first-post.md

5. Once you are satisfied with your post, fire-up the server and check in your brownser to see how it looks:

        hugo server

6. Make sure you commit your changes to the main repo and stash anything left before publishing

7. Publish your new website version with the following command:

        ./deploy.sh "My Commit Message"
