# Consistent Layout

To create a consistent layout across your app, consider the following:

<procedure title="To create a consistent layout across your app, consider the following:" id="create_consistent_layout">
<step>
Define a basic layout file and add the<code-block lang="kotlin">kotlinext.js.require("./globals.css")</code-block> line in it.
</step>
<step>
Reuse this layout in all other files to maintain a consistent design, which will automatically
include <strong>globals.css</strong> file in all your files.
</step>
</procedure>

For reference, you can check the layout file used in the [shadcn-kotlin](https://github.com/dead8309/shadcn-kotlin/blob/cde4b64e1616e632e5660b195145578fa0fe1dd8/site/src/jsMain/kotlin/org/example/kobwebreaxttailwind/components/layouts/PageLayout.kt#L23) project.

<seealso>
<category ref="ext">
<a href="https://tailwindcss.com">Tailwind Docs</a>
</category>
</seealso>
