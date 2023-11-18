<h1>Removing a Submodule in Git</h1>
<p>In Git, submodules allow you to keep a Git repository as a subdirectory of another Git repository. This is a great tool to organize your projects that have dependencies on other projects. However, there might come a time when you want to remove a submodule. Here's how you can do it:</p>

<ol>
    <li>
        <strong>Deinitialize the Submodule:</strong>
        <p>This will remove the working directory of the submodule, but keep the Git directory and the .gitmodules entry.</p>
        <pre><code>git submodule deinit &lt;path_to_submodule&gt;</code></pre>
        <strong>If there were local changes or untracked files:</strong>
        <p>Use the '-f' flag with 'git rm' to forcibly remove the submodule. This will discard local changes and untracked files in the submodule.</p>
        <pre><code>git rm -f &lt;path_to_submodule&gt;</code></pre>
    </li>
    <li>
        <strong>Remove the Submodule Entry:</strong>
        <p>This will remove the entry from the .gitmodules file and remove the submodule's Git directory.</p>
        <pre><code>git rm &lt;path_to_submodule&gt;</code></pre>
    </li>
    <li>
        <strong>Commit the Changes:</strong>
        <p>This step will commit the removal of the submodule from your project.</p>
        <pre><code>git commit -m "Removed &lt;submodule_name&gt; submodule"</code></pre>
    </li>
    <li>
        <strong>Push the Changes:</strong>
        <p>This will push the commit to your remote repository.</p>
        <pre><code>git push</code></pre>
    </li>
 
</ol>
