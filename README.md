# VSCODE remote configs 

This repository contains my configuration for vscode-remote containers. I clone this repo to 
`~/.config/vscode` and then i can create remote workspaces like this:
~~~
{
  "name": "doorman",
  "dockerComposeFile": [
    "${env:HOME}/.config/vscode/development.yml"
  ],
  "workspaceFolder": "${localWorkspaceFolder}",
  "service": "go-development",
  "extensions": [
    "golang.go",
    "humao.rest-client",
    "dline.cobaltnext",
    "sirtori.indenticator",
    "wayou.vscode-todo-highlight",
    "gruntfuggly.todo-tree",
    "eamodio.gitlens",
    "compulim.vscode-clock"
  ]
}
~~~

The `workspaceFolder` is configured to `localWorkspaceFolder` which only works, if you mount the folder from
your local machine to your remote container. You should customize this in the `development.yml` 

