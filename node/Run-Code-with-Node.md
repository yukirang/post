Now is the time to actually take our first look at running code with node.
<h3>Node Console</h3>
First, we need to download and install node from <a href="https://nodejs.org/en/download/">https://nodejs.org/en/download/ </a>

And check the version of node we have, which can also prove that node is installed successfully:
<pre><code>$ node -v
</code></pre>
<pre><code>v8.9.4
</code></pre>
Now we can run some JavaScript code in node:
Start the node runtime:
<pre><code>$ node
</code></pre>
Print something:
<pre><code>&gt; console.log("Helloooooo!");
</code></pre>
<pre><code>Helloooooo!
</code></pre>
<h3>Run a .js file</h3>
Exactly we don't want to type everything in the terminal. Most of the time we run a file in node insdead.
Say I have a file called repeat.js:
<pre><code class="language-javascript">//repeat.js
var repeat = function(word,times){
    for(var i = 0; i &lt; times; i ++){
        console.log(word);
    }
}
repeat("Yes",3);
</code></pre>
And run it with node:
<pre><code>$ node repeat.js
</code></pre>
<pre><code>Yes
Yes
Yes
</code></pre>
Okay, we're done! Super easy isn't it?