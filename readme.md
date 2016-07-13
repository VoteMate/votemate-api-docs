VoteMate API docs
===

## Requirements
- Ruby
- bundler

## Getting started
1. Clone/fork the repo
- `cd` into the repo
- `bundle install`
- `bundle exec middleman server` to run the dev server at `localhost:4567`
- `bundle exec middleman build` to build a production version to the `build` folder

## Editing the API
The entire API is defined in `/data/votemate.yml`. The format is fairly self explanatory.

## Deploying changes
For this, you'll need

- Python
- Ansible
- SSH access to the `votemate.us` server

In the project root, run:

  ansible-playbook -i votemate.us, deploy.yml

All this does is run the middleman build locally and copy the built files over to the server's `/srv/votemate-api-docs` directory.
