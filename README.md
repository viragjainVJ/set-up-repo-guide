# Guide to set up your Repo

### [Basic writing and formatting syntax](https://help.github.com/articles/basic-writing-and-formatting-syntax/)
Create sophisticated formatting for your prose and code on GitHub with simple syntax.

## Issues
- Faced below issue while pushing to remote repo.
```
$ git push -u origin master
Username for 'https://github.com': viragjainVJ
To https://github.com/viragjainVJ/react-draggable-list
 ! [rejected]        master -> master (non-fast-forward)
error: failed to push some refs to 'https://github.com/viragjainVJ/react-draggable-list'
hint: Updates were rejected because the tip of your current branch is behind
hint: its remote counterpart. Integrate the remote changes (e.g.
hint: 'git pull ...') before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.
```
> Use Command :+1: `git push -f origin master` :+1:


## Redux-First Routing
```
npm install --save redux-first-routing
```
Achieve client-side routing the Redux way:

- Read location data from the store.
- Update the location by dispatching navigation actions.
- Let middleware handle the side-effect of history navigation.

![Usage with Universal Router](https://camo.githubusercontent.com/381e787f15ad1f830a41d3e261157ae07d9f3999/687474703a2f2f692e696d6775722e636f6d2f557a51745934542e6a7067)

[Medium FreeCodeCamp](https://medium.freecodecamp.org/an-introduction-to-the-redux-first-routing-model-98926ebf53cb)
