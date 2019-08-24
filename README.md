# Vue JS Wordpress starter for Gridsome

[![Deploy to Netlify](https://www.netlify.com/img/deploy/button.svg)](https://app.netlify.com/start/deploy?repository=https://github.com/gridsome/gridsome-starter-wordpress)



## Install & Todo
Install Gridsome first, then clone repo and run yarn.

Used Bulma CSS direct from cdn in index.html, and custom nav, but can swap out styles for own.
This uses the basics of the Krypto Bulma theme
Just change nav and page templates to yours, header and footer in components folder.
3 pages made, Home, About, and Blog/News
See main.js for imports, put extra plugins in index.js.  DELETE index.html if not required (usually for cdns/font awsome etc)

## Guide

Add your WordPress URL to the plugin options. Already done here, change to required field in gridsome.config and netlify.toml

```js
// gridsome.config.js

module.exports = {
  plugins: [
    {
      use: '@gridsome/source-wordpress',
      options: {
        baseUrl: 'YOUR_WEBSITE_URL', // required
        typeName: 'WordPress', // GraphQL schema name (Optional)
        routes: {
          post: '/:year/:month/:day/:slug', //adds route for "post" post type (Optional)
          post_tag: '/tag/:slug' // adds route for "post_tag" post type (Optional)
        }
      }
    }
  ]
}

```

See all [options](https://gridsome.org/plugins/@gridsome/source-wordpress).

## Included templates

This starter includes basic templates for categories, tags and posts, Home, About and News page.
