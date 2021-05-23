# Animikii Ruby on Rails Templates

This is a central repository for all of Animikii's Rails templates (as well as any associated configuration files and assets). The structure of this repository is that each template has a name ("niiwin" for example), and that name is used for the template itself (`niiwin.rb`), a railsrc file (`niiwin.railsrc`), and optionally a directory with erb files to be used for the template (`niiwin/`).

Generally, the way to use one of the templates is to point to the railsrc file as the value for the `--rc` option when calling `rails new`. This is different than the usual way of applying a template, which is to point to the template directly using the `-m` or `--template` option. The reason for doing it this way is that it allows us to specify options that are required for the template — for example, specifying that Postgres should be used and that Spring should be skipped for Niiwin. The railsrc file includes the template option pointing to the template file, so there's no need to point to it directly. As an example, to create a new rails app, using the niiwin template, you would run:

```sh
$ rails new --rc=https://raw.github.com/animikii/rails_templates/niiwin.railsrc
```
