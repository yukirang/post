<p>I1: Run <pre class="wp-block-preformatted"> npm install webpack</pre>but webpack is still 3.x<br />Solution: May need to specify the version of webpack and install it.</p>
<pre class="wp-block-preformatted">npm install --save-dev webpack@4.0.0
</pre>

<p>I2: Module build failed: TypeError: Cannot read property 'vue' of undefined <br />Solution: Need to update the vue-loader as well.</p>
<pre class="wp-block-preformatted">npm install --save-dev vue-loader
</pre>

<p>I3: Error: cannot find module 'webpack-cli/bin/config-yargs' <br />Solution: This is because in Webpack 4, The CLI moved into a separate package: webpack-cli.</p>
<pre class="wp-block-preformatted">npm install --save-dev webpack-cli
</pre>

<p>I4: TypeError: Cannot destructure property `compile` of 'undefined' or 'null' <br />Solution: Update the webpack-dev-server </p>
<pre class="wp-block-preformatted">npm install --save-dev webpack-dev-server@3.0.0
</pre>

<p>I5: TypeError: compilation.mainTemplate.applyPluginsWaterfall is not a function <br />Solution1: Install the next version of html-webpack-plugin</p>
<pre class="wp-block-preformatted">npm i --save-dev html-webpack-plugin@next
</pre>
<p>Solution2: Install the html-webpack-plugin with yarn</p>
<pre class="wp-block-preformatted">yarn add webpack-contrib/html-webpack-plugin -D
</pre>
<br/>
<p>To be continued...</p>