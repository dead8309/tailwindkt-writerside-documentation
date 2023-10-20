# Installation


**tailwind-kt** is available on [MavenCentral](https://central.sonatype.com/artifact/io.github.dead8309.tailwind-kt/io.github.dead8309.tailwind-kt.gradle.plugin/)

<procedure>
<step>
Add the mavenCentral() to your top-level
<tabs>
<tab title="settings.gradle">
<code-block lang="groovy">
pluginManagement {
    repositories {
        mavenCentral()
    }
}
</code-block>
</tab>
<tab title="build.gradle (legacy)">
<code-block lang="groovy">
buildscript {
    repositories {
        mavenCentral()
    }
}
</code-block>
</tab>
</tabs>
</step>

<step>
Apply the plugin to your project.
<tabs>
<tab title="Kotlin DSL">
<code-block lang="groovy">
// build.gradle.kts
plugins {
    id("io.github.dead8309.tailwind-kt").version("%version%")
}
</code-block>
</tab>
<tab title="Legacy Groovy">
<code-block lang="groovy">
// build.gradle
buildscript {
    ...
    dependencies {
    ...
        classpath 'io.github.dead8309.tailwind-kt:io.github.dead8309.tailwind-kt.gradle.plugin:%version%'
    }
}
apply plugin: "io.github.dead8309.tailwind-kt"
</code-block>
</tab>
</tabs>
</step>
</procedure>