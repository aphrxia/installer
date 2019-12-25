# Laraseat Installer

This document should serves as mini documentation for Laraseat installer command execution.

To use this tool, first you need to install it globally in your system:

```bash
$ composer require aphrxia/installer
```

## Commands

What this tool provide is a numbers of custom new options to create your Laravel project boilerplate. Those options are:

### Project type

`$ laravel create:<type> <name>`

Instead of just using `new` (standard and well known Laravel project initialization syntax), we came up with `create:<type>` command which can be used to identify your project type that will determine how your project will created and structurized for you. There are two type known to this installer, `api` and `web`.

#### API Projects command parameter and options

`$ laravel create:api my_backend_project`

When creating as an API backend project, the installer will give you bare-bone, lightweight, ready-to-go project structure. It will leave out stuff mostly don't needed when developing pure backend applications, while keep it possible to customise it further based on your needs. One way to do the customisation is to utilize some automated fine-tuning features provided by the installer itself, like automatic install and setup Laravel Password and do necessary Laravel setup to implement API versioning into your project:

`$ laravel create:api my_backend_project --use-passport --use-versioning`

There are several other useful options you might use, feel free to explore them below:

| Parameter | Default |   |
| --------- | ------- | -- |
| `--create-test-env` | N/A | Will create `.test.env` with some default configurations for your testing purposes. |
| `--use-strict-cookie` | N/A | Setup mechanism needed to implement secure HTTP cookie for API consuming purposes. |
| `--use-passport` | N/A | Install and init Laravel Passport package for API client authentication. |
| `--use-versioning` | N/A | Setup and implement API versioning. |
| `--with-apidoc` | N/A | Setup apidoc package for API documentation. |
| `--with-gs-bddflow` | N/A | Install and setup `laravel-gs-bddflow` package for BDD style project. |
| `--with-gs-gitflow` | N/A | Install and setup `laravel-gs-gitflow` package for Git development flow. |
| `--dockerized` | N/A | Create Docker files needed to convert this project into Docker container. |
| `--serve` | N/A | Auto run the project. If it has been dockerized, this command will trigger container creation and then run them. |
| `--port` | `8000` | Specify local port for current project instance when its run. |
| `--watch` | N/A | **Experimental**: watch the filesystem change inside current project and relaunch everything if there is any. |
