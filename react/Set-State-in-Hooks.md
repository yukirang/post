


<!-- wp:paragraph -->
<p>In React, when we want to update the state variable under the class, we can use <code>this.setState</code>&nbsp;, which automatically merges the update objects so that we just need to put which state and what value we want to modify:</p>
<!-- /wp:paragraph -->

<!-- wp:html -->
<pre>this.state = {
  user: username,
  pwd: password
}
...

this.setState({ user: username, pwd: password })  

const onChange = e =&gt; this.setState({pwd: e.target.value});</pre>
<!-- /wp:html -->

<!-- wp:paragraph -->
<p>After the <code>onChange()</code> is triggered, the <code>setState()</code> will change the <code>pwd</code> state and lead to a re-render. </p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Suppose now we are using the Hooks, which enables a function component to add some state. the <code>useState</code> returns both the&nbsp;state value and the state update function.&nbsp; Say we name the update function "setState". We still want to change the <code>pwd</code> (in this case it's a prop under the state object <code>myState</code>).</p>
<!-- /wp:paragraph -->

<!-- wp:html -->
<pre class="wp-block-preformatted">const [myState, setState] = useState({ user: '',pwd: ''});

const onChange = e =&gt; this.setState({pwd: e.target.value});
</pre>
<!-- /wp:html -->

<!-- wp:paragraph -->
<p>Then we will lose the <code>user</code> string and only have the <code>pwd</code> inside <code>myState</code>!</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Unlike&nbsp;<code>this.setState</code> in a class component, the return function of <code>useState</code> will replace the state object with the new one, instead of merging them!</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>So we may want to use the <strong>spread operator</strong> to replicate the original object and then overwrite the props:</p>
<!-- /wp:paragraph -->

<!-- wp:preformatted -->
<pre class="wp-block-preformatted">const onChange = e =&gt; setState( {...myState, pwd: e.target.value;} )</pre>
<!-- /wp:preformatted -->

<!-- wp:paragraph -->
<p>Or we can split the component state into different parts:</p>
<!-- /wp:paragraph -->

<!-- wp:preformatted -->
<pre class="wp-block-preformatted">const [myState, setUser] = useState({ user: '',pwd: ''});

const [myState, setPwd] = useState({ user: '',pwd: ''});</pre>
<!-- /wp:preformatted -->

<!-- wp:paragraph -->
<p>And then update them separately.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Another thing to notice is that, when using a Hook, if the new value is the same as the current state, React won’t trigger a re-render:<br></p>
<!-- /wp:paragraph -->

<!-- wp:preformatted -->
<pre class="wp-block-preformatted">onChange={e =&gt; {
          myState.pwd = e.target.value;
          setState(myState); 
 }}</pre>
<!-- /wp:preformatted -->

<!-- wp:paragraph -->
<p>So we need a new object to trigger the re-render.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Hope you enjoy!</p>
<!-- /wp:paragraph -->