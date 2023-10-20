# Usage

To use the tailwind-kt plugin follow these steps:

> The plugin generates necessary files when you start your app for the first time. No manual file creation required. You can customize default values later to match your requirements.
>
{style="note"}

#### Configure tailwind { } block.

The tailwind-kt plugin offers configuration options that can be customised through the
`tailwind {}` block in your build.gradle. Although it is **optional and not necessary in
most cases**, you can adjust the default settings according to your requirements
.Refer to [TailwindPluginExtension](Extensions.md#tailwindpluginextension) for more details

```groovy
     tailwind {
        configDir.set(rootDir.resolve("my_configs_dir"))
        moduleName.set("my_module_name")
     }
```


#### setupTailwindProject()

In your `kotlin` block use `setupTailwindProject()` function.

```groovy
   kotlin {
     setupTailwindProject()
     // ...
   }
```

The `setupTailwindProject()` function performs the following:
<procedure>
<step>
Sets up the <strong>Js(IR)</strong> target with webpack settings to enable CSS support.
</step>
<step>
Installs necessary npm dependencies:
<ul>
        <li>tailwindcss: <strong>%tailwind-version%</strong></li>
        <li>postcss: <strong>%postcss-version%</strong></li>
        <li>autoprefixer: <strong>%autoprefixer-version%</strong></li>
        <li>postcss-loader: <strong>%postcssloader-version%</strong></li>
</ul>
</step>
<step>
Adds the following dependency:
<strong>org.jetbrains.kotlin-wrappers:kotlin-extensions:1.0.1-pre.256-kotlin-1.5.31</strong>
</step>
</procedure>
   
#### Skipping Dependencies
You can skip installing **npm** dependencies by passing `skipDependencies = true` when calling `setupTailwindProject()`.

> The `kotlin-extensions` dependency will always be installed as it is necessary to include your CSS file.

> Make sure to add 
> ```kotlin
> kotlinext.js.require("./globals.css")
> ```
> in the entry point of your application, such as `main` function.
> 
{style="note"}

> If the `globals.css` file doesn't exist in `resources/globals.css`,the plugin will provide a default one

🎉 Now you can start using tailwind classes in your application.