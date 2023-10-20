# Tasks

> In the context of these tasks, **`$$configDir`** represents the value you have set in the **`tailwind {}`** extension's **`configDir`** field, 
> or if you haven't set it, its value will be the default value (**`project.projectDir`**). Similarly, **`$$moduleName`** represents the value of the **`moduleName`** field in the **`tailwind {}`** extension.
>
{style="note"}

#### copyConfigFiles

This task copies `tailwind.config.js` and `postcss.config.js` from `$$configDir` to `buildDir/js/packages/$$moduleName`.
It runs after every `compileKotlinJs` task and depends on [generateDefaultFiles](#generatedefaultfiles) task


#### generateDefaultFiles

This task generates the following files if they don't already exist to prevent overwriting your configurations:


| File/Folder name         | Location                                       |
|--------------------------|------------------------------------------------|
| tailwind.config.js       | `$$configDir`                                  |
| postcss.config.js        | `$$configDir`                                  |
| globals.css              | `./src/jsMain/resources/`                      |
| webpack.config.d         | `./webpack.config.d/` <br/>(project directory) |
| postcss-loader.config.js | `./webpack.config.d/postcss-loader.config.js`  |

> The `./` notation refers to the project directory in which the plugin is applied.
