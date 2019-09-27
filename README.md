<!-- AUTO-GENERATED-CONTENT:START (STARTER) -->
<p align="center">
  <a href="junior.house">
    <img alt="Das House Ooh Yah" src="./content/assets/bandit.png" width="60" />
  </a>
</p>
<h1 align="center">
  The Junior House Blog
</h1>

This repository builds directly into the blog located at `http://www.junior.house` and written by Ryan Othniel Kearns, Alex Langshur, and Harry Mellsop. For instructions on how to configure your local environment for posting, read what's immediately below! For a writeup on how this blog was built, check back on this document soon!

## Local Environment Configuration

1. **Navigate to your Desired Directory Endpoint**

    For me, this is `~/Desktop/code`, so I would replace `${dirname}` in the below example with `~/Desktop/code`.

    ```shell
    cd ${dirname}
    ```

    Later on we'll set up an alias that references this endpoint. New blog posts don't require any manipulation of the source code or the directory at all, so just put it somewhere it won't be fussed with.

1.  **Clone this Repository**

    ```shell
    git clone https://github.com/Junior-House/blog.git
    ```

1.  **Gotta install those Packarinos**

    ```shell
    cd blog
    npm install
    ```

1.  **Start Developing**

    To run a development build of the blog:

    ```shell
    gatsby develop
    ```

    The site runs at `http://localhost:8000`.

    _Note: You'll also see a second link: _`http://localhost:8000/___graphql`_. This is a tool you can use to experiment with querying your data. Learn more about using this tool in the [Gatsby tutorial](https://www.gatsbyjs.org/tutorial/part-five/#introducing-graphiql)._

1.  **Set up environmental variables**

    Copy the following into your `~/.bash_profile`, where `${yourname}` is replaced with the name your blog posts will be authored with. Mine is `Ryan Othniel Kearns`.

    ```shell
    export MYNAME="${yourname}"
    ```

    Also copy the following into your `~/.bash_profile`, where `${dirname}` is replaced with your choice in the first instruction:

    ```shell
    alias posthard="${dirname}/blog/post-hard"
    ```

    Setting this alias will allow you to `posthard` from anywhere on your computer! If you've set it up right, running the alias (after terminal restart) should prompt you for a blog post title, then open vim to write the post.

## Additional notes about the Gatsby boilerplate build

A quick look at the top-level files and directories you'll see in a Gatsby project.

    .
    ├── node_modules
    ├── src
    ├── .gitignore
    ├── .prettierrc
    ├── gatsby-browser.js
    ├── gatsby-config.js
    ├── gatsby-node.js
    ├── gatsby-ssr.js
    ├── LICENSE
    ├── package-lock.json
    ├── package.json
    └── README.md

1.  **`/node_modules`**: This directory contains all of the modules of code that your project depends on (npm packages) are automatically installed.

2.  **`/src`**: This directory will contain all of the code related to what you will see on the front-end of your site (what you see in the browser) such as your site header or a page template. `src` is a convention for “source code”.

3.  **`.gitignore`**: This file tells git which files it should not track / not maintain a version history for.

4.  **`.prettierrc`**: This is a configuration file for [Prettier](https://prettier.io/). Prettier is a tool to help keep the formatting of your code consistent.

5.  **`gatsby-browser.js`**: This file is where Gatsby expects to find any usage of the [Gatsby browser APIs](https://www.gatsbyjs.org/docs/browser-apis/) (if any). These allow customization/extension of default Gatsby settings affecting the browser.

6.  **`gatsby-config.js`**: This is the main configuration file for a Gatsby site. This is where you can specify information about your site (metadata) like the site title and description, which Gatsby plugins you’d like to include, etc. (Check out the [config docs](https://www.gatsbyjs.org/docs/gatsby-config/) for more detail).

7.  **`gatsby-node.js`**: This file is where Gatsby expects to find any usage of the [Gatsby Node APIs](https://www.gatsbyjs.org/docs/node-apis/) (if any). These allow customization/extension of default Gatsby settings affecting pieces of the site build process.

8.  **`gatsby-ssr.js`**: This file is where Gatsby expects to find any usage of the [Gatsby server-side rendering APIs](https://www.gatsbyjs.org/docs/ssr-apis/) (if any). These allow customization of default Gatsby settings affecting server-side rendering.

9.  **`LICENSE`**: Gatsby is licensed under the MIT license.

10. **`package-lock.json`** (See `package.json` below, first). This is an automatically generated file based on the exact versions of your npm dependencies that were installed for your project. **(You won’t change this file directly).**

11. **`package.json`**: A manifest file for Node.js projects, which includes things like metadata (the project’s name, author, etc). This manifest is how npm knows which packages to install for your project.

12. **`README.md`**: A text file containing useful reference information about your project.