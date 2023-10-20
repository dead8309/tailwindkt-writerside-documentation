# Extensions

The tailwind-kt plugin provides the following extension for configuration:

#### TailwindPluginExtension
These values can be configured through `tailwind {}` block in your `build.gradle` file.

| Field        | Type               | Description                                                                                                                                                                                            | Default              |
|--------------|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------|
| `configDir`  | `Property<File>`   | The folder containing *tailwind.config.js* and *postcss.config.js* files.                                                                                                                              | `project.projectDir` |
| `moduleName` | `Property<String>` | The name of the folder where the build files packages are located. For most projects this corresponds to the folder under `build/js/packages/[rootProject.name]` in the root directory of your project | `rootProject.name`   |

