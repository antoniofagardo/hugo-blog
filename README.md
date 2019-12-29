## Cloning repo with submodules

    git clone https://github.com/antoniofagardo/hugo-blog.git --recurse-submodules

## Publishing new website version

    ./deploy.sh "My Commit Message"

## Adding a new theme

    git submodule add https://github.com/nirocfz/arabica themes/arabica

## Start dev server

    hugo server

## Adding a new post

    hugo new post/my-first-post.md
