<strong>What is NPM?</strong>

Here's the definition[1]:
<blockquote>npm is the package manager for JavaScript and the world’s largest software registry. Discover packages of reusable code — and assemble them in powerful new ways.</blockquote>
<strong>Why do we care about it?</strong>

We might feel it annoying writing some common but time-consuming codes every time by ourselves. Don't worry about it because there's always someone else who has done it for us. All we need to do is to stand on there shoulder and continue our work easily. Even if we find no one has done it before, we can still write our own package and make it reusable by putting it somewhere. That's why we need npm.

<strong>How to use?</strong>

Initialize your project with a package.json

A package.json file is like a central guide and declaration for your project.  Normally if you are working with a JavaScript project you need to include a package.json file.

Normally[2]
<blockquote>A <code class="highlighter-rouge">package.json</code> file:
<ul>
 	<li>lists the packages your project depends on</li>
 	<li>specifies versions of a package that your project can use using <a href="https://docs.npmjs.com/about-semantic-versioning">semantic versioning rules</a></li>
 	<li>makes your build reproducible, and therefore easier to share with other developers</li>
</ul>
</blockquote>
And the initialization command is:

<code>$ npm init</code>

Install a new package: <strong>npm install &lt;package&gt;</strong>

<code>$ npm install simple-react-color-picker
</code>

<strong>--save</strong>

If you run this with the install, it will add the needed description of dependency  for the package in package.json as well.

<code>$ npm install simple-react-color-picker --save</code>

Update a package to the latest version: <strong>npm update &lt;package&gt;</strong>

<code>$ npm update simple-react-color-picker</code>

List all packages installed:

<code>$ npm ls</code>

&nbsp;

References:

[1]"npm", <i>Npmjs.com</i>, 2018. [Online]. Available: https://www.npmjs.com/. [Accessed: 12- Nov- 2018].

[2]<i>Docs.npmjs.com</i>, 2018. [Online]. Available: https://docs.npmjs.com/creating-a-package-json-file. [Accessed: 12- Nov- 2018].