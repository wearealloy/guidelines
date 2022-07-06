# Getting Started

## Development environment configuration for projects with Craft CMS

A simple option for starting a Craft CMS project is to create a local development environment that meets [the minimum CMS requirements](https://craftcms.com/docs/4.x/requirements.html). 

There are several recipes and flavors for putting together a local development environment focused on Craft CMS. At Black Magic, we use the following technologies: 

### Laravel Valet

Laravel Valet, as a local server running Nginx, allowing to use virtual hosts with the ```.test``` domain. 

Out of the box, **Valet supports different types of CMS and webapps such as WordPress, Symfony and many more**.

Follow Valet's official [documentation for installation and configuration](https://laravel.com/docs/9.x/valet).

> :warning: **Warning:** We do not recommend using MAMP or similar tools because they may generate undesired behavior with any of the following suggested tools.

### Composer

Composer is the dependency manager of Craft CMS. It is important that you install Composer globally before installing Craft. 

Follow the [Composer documentation to install globally](https://getcomposer.org/doc/00-intro.md#globally). 


[Return](../README.md)