# deep-sea-currents

Here lays the flow (GitHub actions) which turns the sea (CI pipeline) and fills sails with wind to guide them from port to port (CD pipeline)

This actions script will handle any steps in the coopstools-homebrew org that require the use of secrets or other sensitive info.

## CI

This library will update the tags on a repo, following a the standard:

//TODO: Add rules around updating of tags

It will also build and push a docker image for the repo in which it is used. The newly created tag can be found in the outputs as `tag`.

## CD

Currently, this library does not handle CD steps. Though, the intension is to let this action be in charge of updating the k8s_deployment repo, either creating a new dev env (if the branch name matches `dev-*`), or creating a PR to `main` if it's on the `main` branch.
