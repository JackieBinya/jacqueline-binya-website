
This project is a personal website portfolio
 
 ### Stack
This site was created using [Hugo](https://gohugo.io/). The Hugo theme [anubis](https://themes.gohugo.io/hugo-theme-anubis/) was used to bootstrap the project.

The theme is imported into the project as a sub-module. A sub-module is a git repository contained in another git repository. These two repositories then have what can be loosely described as a parent-child relationship.All the sub-modules can then be tracked from the parent repository. A submodule can be located anywhere in a parent Git repository’s working directory and is configured via a .gitmodules file located at the root of the parent repository.

## Fresh Install guide
Run the commands below in you terminal to get started with a fresh install.

    1. `git clone --recursive <URL of this directory`: this command will allow you to pull both the parent repo and sumb-module simultenously.
    2. cd <PROJECT> && `rm -rf public`
    3. `git rm --cached public`
    4. `git submodule add -b master https://github.com/<USERNAME>/<USERNAME>.github.io.git public`
    5. To start the hugo server locally run the command `hugo server` on the terminal.



