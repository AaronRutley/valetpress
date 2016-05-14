# ValetPress

Experimental tool to create WordPress sites quickly with [Valet](https://laravel.com/docs/5.2/valet)

This is a similar concept to the [VV](https://github.com/bradp/vv) site wizard.

With this tool I was able to:

- Create a new, empty WP site (with database setup) in **4.7 seconds**.
- Create a new WP dev site with my starter repo (plugins and theme) in **28 seconds**.

## To install

- Install [Valet](https://laravel.com/docs/5.2/valet)  
- Install [WP-CLI](https://wp-cli.org/)
- Download / Clone this repo into a directory like `~/.valetpress`
- Customise / Extend the `valetpress` file as needed to suit your projects
- Include the `valetpress` script in your `.bashrc` or similar file.

Note: I'm including this in my `.zshrc` file as I'm using [oh-my-zsh](https://github.com/robbyrussell/oh-my-zsh).

```
if [ -f ~/.valetpress/valetpress ]; then
    source ~/.valetpress/valetpress
else
    print "404: ~/.valetpress/valetpress not found."
fi
```

## Available Commands:

`vp empty`

- Will ask for the name of your project, enter something like `myproject`.
- Download WordPress into a directory like `~/Sites/myproject`
- Setup the database called `myproject` & configure the install
- Create a user `myproject` with a temp password of `password`
- Remove the default plugins and themes (leaves twentysixteen)
- Have `myproject.dev` running in just a few seconds

`vp clone`

- Will ask for the name of your project, enter something like `myproject`.
- Download WordPress into a directory like `~/Sites/myproject`
- Setup the database called `myproject` & configure the install
- Create a user `myproject` with a temp password of `password`
- Remove the `wp-content` directory
- Ask you to enter a URL for the git repo
- Clone the repo into `wp-content`
- Update and activate all plguins
- Have `myproject.dev` running in just a few seconds


`vp create`
- Will ask for the name of your project
- Clone down a starter repo, run `npm install` & run `gulp`.
- (At the moment this is very custom to my workflow It's best you customise this for your own use)

`vp start`
- Will list all projects in your `~/Sites` directory and ask you to choose one
- Backup the database
- Update WP core and plugins with WP-CLI
- Navigate to the theme folder (if it matches the project name)
- Start gulp
- (It's best you customise this for your own use)

`vp delete`
- Will ask for the name of the project you would like to delete
- Ask you to confim you wish to delete the project
- Delete the database for that project
- Delete the directory for that project

`vp help`
- Will display a summary of available commands

##  Notes
- This is very much a proof of concept at the moment
- If there's interest I'll make this script into a tool that's easier to install
- Hit me up here on github, twitter or email if you're interested in helping out!

