<h1>Base AngularJS Application</h1>

<p>In command-line go to the project folder.</p>

<h2>Install npm</h2>
<pre>npm install</pre>

<h2>Install bower</h2>
<p>Because Bower is using Git repository, run it in Git bash command-line.</p>
<pre>bower install</pre>

<h2>Run default Grunt task</h2>
<pre>grunt</pre>

<h2>E2E Tests</h2>
<h3>Setup</h3>
<pre>npm install -g protractor</pre>
<pre>webdriver-manager update</pre>
<pre>webdriver-manager start</pre>

<h3>Configuration</h3>
<b>protractor.conf.js</b>
<pre>
exports.config = {
  allScriptsTimeout: 11000,

  specs: [
    'e2e-basic.js'
  ],

  capabilities: {
    'browserName': 'chrome'
  },

  baseUrl: 'http://localhost:1338',

  framework: 'jasmine',

  jasmineNodeOpts: {
    defaultTimeoutInterval: 30000
  }
};
</pre>

<h3>Run tests</h3>
<pre>protractor e2e-basic.js</pre>