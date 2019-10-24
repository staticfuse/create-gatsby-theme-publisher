# Create Gatsby WordPress Publisher Theme

![Gatsby Theme Publisher Screenshot](https://data.staticfuse.com/wp-content/uploads/2019/10/publisher-hero.jpg)

A Gatsby starter that has the [Gatsby Theme Publisher](https://github.com/staticfuse/gatsby-theme-publisher) installed and preconfigured.

For a full tutorial, please see our article on [headless WordPress with Gatsby](https://staticfuse.com/blog/how-to-build-headless-wordpress-sites-with-gatsby/).

### Example Sites

These sites all use the Publisher theme with WordPress as the backend.

- [staticfuse.com](https://staticfuse.com)
- [scottbolinger.com](https://scottbolinger.com)
- [demo site](https://publisher.staticfuse.com)

### Prequisites

- [Node and NPM](https://www.gatsbyjs.org/tutorial/part-zero/#-install-nodejs-and-npm)
- [Yarn](https://yarnpkg.com/lang/en/docs/install/)

### Overview

1.  Clone this repo: `git clone https://github.com/staticfuse/create-gatsby-theme-publisher.git`
2.  cd into the folder `cd create-gatsby-theme-publisher` (You can change the project folder name, and theme name in package.json)
3.  Install dependencies `yarn`
4.  Install [WPGraphQL plugin on your WordPress site](https://github.com/wp-graphql/wp-graphql)
5.  Configure your site options in [gatsby-config.js](https://github.com/staticfuse/create-gatsby-theme-publisher/blob/master/gatsby-config.js) Explanation of the options is [below](https://github.com/staticfuse/create-gatsby-theme-publisher#publisher-theme-options)
6.  Start the demo site `gatsby develop`
7.  Add your logo and [customize the theme](https://github.com/staticfuse/create-gatsby-theme-publisher#theme-customization)
8.  [Publish to Netlify](https://github.com/staticfuse/create-gatsby-theme-publisher#publishing-to-netlify) or any static host.

## Adding Gatsby WordPress Theme Publisher to an existing Gatsby site

1. `yarn add @staticfuse/gatsby-theme-publisher` or `npm install @staticfuse/gatsby-theme-publisher`
2. In your `gatsby-config.js` :
```js
module.exports = {
  siteMetadata: {
    title: 'Static Fuse',
    description: 'Headless WordPress with Gatsby FTW.',
    author: 'Scott and Justin',
    twitter: '@staticfuse',
    siteUrl: `https://staticfuse.com`,
  },
  plugins: [
    {
      resolve: `@staticfuse/gatsby-theme-publisher`,
      options: {
        starterPages: true, // add a customizable home, about, and contact page
        mailChimpEndpoint: 0, // https://www.gatsbyjs.org/packages/gatsby-plugin-mailchimp/#mailchimp-endpoint
        dynamicComments: 1, // enable comments
        gaTrackingId: 0, // google analytics tracking
        wordPressUrl: `https://mywpinstall.com`, // The url of your WordPress install
        blogURI: '/blog' // The page to display your posts
      },
    },
  ],
}
```

## Publisher Theme Options

For theme options, customization, and more, please view the [main readme file here](https://github.com/staticfuse/gatsby-theme-publisher).
