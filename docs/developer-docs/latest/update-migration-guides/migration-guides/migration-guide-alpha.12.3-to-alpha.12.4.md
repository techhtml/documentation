---
title: Migrate from alpha.12.3 to alpha.12.4 - Strapi Developer Docs
description: Learn how you can migrate your Strapi application from alpha.12.3 to alpha.12.4.
canonicalUrl: https://docs.strapi.io/developer-docs/latest/update-migration-guides/migration-guides/migration-guide-alpha.12.3-to-alpha.12.4.html
---

# Migration guide from alpha.12.3 to alpha.12.4

**Here are the major changes:**

- Add search to content manager
- Add bulk actions in content-manager
- Add Enumeration type to Content-Type Builder

**Useful links:**

- Changelog: [https://github.com/strapi/strapi/releases/tag/v3.0.0-alpha.12.4](https://github.com/strapi/strapi/releases/tag/v3.0.0-alpha.12.4)
- GitHub diff: [https://github.com/strapi/strapi/compare/v3.0.0-alpha.12.3...v3.0.0-alpha.12.4](https://github.com/strapi/strapi/compare/v3.0.0-alpha.12.3...v3.0.0-alpha.12.4)

<br>

::: tip
Feel free to [join us on Slack](http://slack.strapi.io) and ask questions about the migration process.
:::

<br>

## Getting started

Install Strapi `alpha.12.4` globally on your computer. To do so run `npm install strapi@3.0.0-alpha.12.4 -g`.

When it's done, generate a new empty project `strapi new myNewProject` (don't pay attention to the database configuration).

<br>

## Update node modules

Update the Strapi's dependencies version (move Strapi's dependencies to `3.0.0-alpha.12.4` version) of your project.

Run `npm install strapi@3.0.0-alpha.12.4 --save` to update your strapi version and then run the same command for `strapi-mongoose` or `strapi-bookshelf` depending on the module you use in your application.

<br>

## Update the Admin

::: tip
If you performed updates in the Admin, you will have to manually migrate your changes.
:::

Delete your old admin folder and replace it with the new one.

<br>

## Update the Plugins

::: tip
If you did a custom update on one of the plugins, you will have to manually migrate your update.
:::

Copy the fields and relations you had in your `/plugins/users-permissions/models/User.settings.json` and `/plugins/users-permissions/config/jwt.json` file in the new one.

Then, delete your old `plugins` folder and replace it with the new one.

<br>

That's all, you have now upgraded to Strapi `alpha.12.4`.
