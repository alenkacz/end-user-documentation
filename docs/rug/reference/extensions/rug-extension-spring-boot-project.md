## Type: `SpringBootProject`

**Spring Boot project**

### `SpringBootProject` Operations

#### Operation: `addDirectory`

Create a directory

##### Parameters

| Name        | Type           | Description  |
| ------------|:---------------|:-------------|
| ***name*** | `class java.lang.String` | *The name of the directory being added* |
| ***parentPath*** | `class java.lang.String` | *The path under which the directory should be created* |

#### Operation: `addDirectoryAndIntermediates`

Create a directory

##### Parameters

| Name        | Type           | Description  |
| ------------|:---------------|:-------------|
| ***directoryPath*** | `class java.lang.String` | *The path under which the directory and any missing intermediate directories will be created* |

#### Operation: `addExecutableFile`

Add the given executable file to the project. Path can contain /s. Content is a literal string

##### Parameters

| Name        | Type           | Description  |
| ------------|:---------------|:-------------|
| ***path*** | `class java.lang.String` | *The path to use* |
| ***content*** | `class java.lang.String` | *The content to be placed in the new file* |

#### Operation: `addFile`

Add the given file to the project. Path can contain /s. Content is a literal string

##### Parameters

| Name        | Type           | Description  |
| ------------|:---------------|:-------------|
| ***path*** | `class java.lang.String` | *The path to use* |
| ***content*** | `class java.lang.String` | *The content to be placed in the new file* |

#### Operation: `annotateBootApplication`

Add the given annotation to the Spring Boot application class

##### Parameters

| Name        | Type           | Description  |
| ------------|:---------------|:-------------|
| ***pkg*** | `class java.lang.String` | *The package of the annotation* |
| ***annotationName*** | `class java.lang.String` | *The annotation to add* |

#### Operation: `applicationClassFQN`

The FQN of the Spring Boot Application class

##### Parameters

*None*

#### Operation: `applicationClassPackage`

The package the Spring Boot Application class is in

##### Parameters

*None*

#### Operation: `applicationClassSimpleName`

The simple name of the Spring Boot Application class

##### Parameters

*None*

#### Operation: `backingArchiveProject`

Return a new Project View based on the original backing object (normally the .atomist/ directory)

##### Parameters

*None*

#### Operation: `blockingProblem`

Report a severe, blocking problem

##### Parameters

| Name        | Type           | Description  |
| ------------|:---------------|:-------------|
| ***msg*** | `class java.lang.String` | *The message to be displayed* |
| ***arg1*** | `com.atomist.rug.runtime.rugdsl.FunctionInvocationContext<?>` | ** |

#### Operation: `children`

Children

##### Parameters

*None*

#### Operation: `context`

Provides access additional context, such as the PathExpressionEngine

##### Parameters

*None*

#### Operation: `copyEditorBackingFileOrFail`

Copy the given file from the editor's backing archive. Fail the editor if it isn't found or if the destination already exists

##### Parameters

| Name        | Type           | Description  |
| ------------|:---------------|:-------------|
| ***sourcePath*** | `class java.lang.String` | *Source path* |
| ***destinationPath*** | `class java.lang.String` | *Destination path* |

#### Operation: `copyEditorBackingFileOrFail`

Copy the given file from the editor's backing archive to the same path in project being edited. Fail the editor if it isn't found or if the destination already exists

##### Parameters

| Name        | Type           | Description  |
| ------------|:---------------|:-------------|
| ***sourcePath*** | `class java.lang.String` | *Source path* |

#### Operation: `copyEditorBackingFilesOrFail`

Copy the given file from the editor's backing archive. Fail the editor if it isn't found or if the destination already exists

##### Parameters

| Name        | Type           | Description  |
| ------------|:---------------|:-------------|
| ***sourcePath*** | `class java.lang.String` | *Source directory* |
| ***destinationPath*** | `class java.lang.String` | *Destination path* |

#### Operation: `copyEditorBackingFilesPreservingPath`

Copy the given files from the editor's backing archive under the given directory into the same directory in the project being edited.

##### Parameters

| Name        | Type           | Description  |
| ------------|:---------------|:-------------|
| ***sourcePath*** | `class java.lang.String` | *Source directory* |

#### Operation: `copyEditorBackingFilesWithNewRelativePath`

Copy the given files from the editor's backing archive under the given path. Take the relative paths and place under new destination path

##### Parameters

| Name        | Type           | Description  |
| ------------|:---------------|:-------------|
| ***sourcePath*** | `class java.lang.String` | *Source directory* |
| ***destinationPath*** | `class java.lang.String` | *Destination path* |

#### Operation: `copyFile`

Copy the given file in the target project. It is not an error if it doesn't exist

##### Parameters

| Name        | Type           | Description  |
| ------------|:---------------|:-------------|
| ***sourcePath*** | `class java.lang.String` | *Source path* |
| ***destinationPath*** | `class java.lang.String` | *Destination path* |

#### Operation: `copyFileOrFail`

Copy the given file in the target project. Fail the editor if it isn't found or if the destination already exists

##### Parameters

| Name        | Type           | Description  |
| ------------|:---------------|:-------------|
| ***sourcePath*** | `class java.lang.String` | *Source path* |
| ***destinationPath*** | `class java.lang.String` | *Destination path* |

#### Operation: `countFilesInDirectory`

The number of files directly in this directory

##### Parameters

| Name        | Type           | Description  |
| ------------|:---------------|:-------------|
| ***path*** | `class java.lang.String` | *The path to use* |

#### Operation: `deleteDirectory`

Deletes a directory with the given path

##### Parameters

| Name        | Type           | Description  |
| ------------|:---------------|:-------------|
| ***path*** | `class java.lang.String` | *The path to use* |

#### Operation: `deleteFile`

Delete the given file from the project. Path can contain /s.

##### Parameters

| Name        | Type           | Description  |
| ------------|:---------------|:-------------|
| ***path*** | `class java.lang.String` | *The path to use* |

#### Operation: `describeChange`

Describe a change we made to this object

##### Parameters

| Name        | Type           | Description  |
| ------------|:---------------|:-------------|
| ***arg0*** | `class java.lang.String` | ** |

#### Operation: `directoryExists`

Does a directory with the given path exist?

##### Parameters

| Name        | Type           | Description  |
| ------------|:---------------|:-------------|
| ***path*** | `class java.lang.String` | *The path to use* |

#### Operation: `editWith`

Edit with the given editor

##### Parameters

| Name        | Type           | Description  |
| ------------|:---------------|:-------------|
| ***editorName*** | `class java.lang.String` | *Name of the editor to invoke* |
| ***params*** | `class java.lang.Object` | *Parameters to pass to the editor* |

#### Operation: `eval`

Evaluate, i.e., compile and execute, JavaScript code.

##### Parameters

| Name        | Type           | Description  |
| ------------|:---------------|:-------------|
| ***arg0*** | `class java.lang.Object` | ** |

#### Operation: `fail`

Cause the operation to fail with a fatal error

##### Parameters

| Name        | Type           | Description  |
| ------------|:---------------|:-------------|
| ***msg*** | `class java.lang.String` | *The message to be displayed* |

#### Operation: `fileContains`

Does a file with the given path exist and have the expected content?

##### Parameters

| Name        | Type           | Description  |
| ------------|:---------------|:-------------|
| ***path*** | `class java.lang.String` | *The path to use* |
| ***content*** | `class java.lang.String` | *The content to check* |

#### Operation: `fileCount`

Return the number of files in this project

##### Parameters

*None*

#### Operation: `fileExists`

Does a file with the given path exist?

##### Parameters

| Name        | Type           | Description  |
| ------------|:---------------|:-------------|
| ***path*** | `class java.lang.String` | *The path to use* |

#### Operation: `fileHasContent`

Does a file with the given path exist and have the expected content?

##### Parameters

| Name        | Type           | Description  |
| ------------|:---------------|:-------------|
| ***path*** | `class java.lang.String` | *The path to use* |
| ***content*** | `class java.lang.String` | *The content to check against the given file* |

#### Operation: `files`

Files in this archive

##### Parameters

*None*

#### Operation: `findFile`

Find file with the given path. Return null if not found.

##### Parameters

| Name        | Type           | Description  |
| ------------|:---------------|:-------------|
| ***path*** | `class java.lang.String` | *Path of the file we want* |

#### Operation: `isMaven`

Is this a Maven project?

##### Parameters

*None*

#### Operation: `isSpring`

Is this a Spring project?

##### Parameters

*None*

#### Operation: `isSpringBoot`

Is this a Spring Boot project?

##### Parameters

*None*

#### Operation: `javaFileCount`

Return the number of Java files in this module

##### Parameters

*None*

#### Operation: `majorProblem`

Report a major problem

##### Parameters

| Name        | Type           | Description  |
| ------------|:---------------|:-------------|
| ***msg*** | `class java.lang.String` | *The message to be displayed* |
| ***arg1*** | `com.atomist.rug.runtime.rugdsl.FunctionInvocationContext<?>` | ** |

#### Operation: `merge`

Merge the given template to the given output path.

##### Parameters

| Name        | Type           | Description  |
| ------------|:---------------|:-------------|
| ***template*** | `class java.lang.String` | *The name of the template within the backing Rug archive, under /.atomist / templates* |
| ***path*** | `class java.lang.String` | *The path that will be the merged path within the output project.* |
| ***parameters*** | `class java.lang.Object` | *Parameters* |

#### Operation: `mergeTemplates`

Merge templates from the specified directory in the backing archive, under /.atomist/templates, to the given output path in the project being edited.

##### Parameters

| Name        | Type           | Description  |
| ------------|:---------------|:-------------|
| ***templatesPath*** | `class java.lang.String` | *Source template path where content will be used to merge into target project* |
| ***outputPath*** | `class java.lang.String` | *The destination path within the destination project* |
| ***ic*** | `class java.lang.Object` | *Parameters to the template* |

#### Operation: `minorProblem`

Report a minor problem

##### Parameters

| Name        | Type           | Description  |
| ------------|:---------------|:-------------|
| ***msg*** | `class java.lang.String` | *The message to be displayed* |
| ***arg1*** | `com.atomist.rug.runtime.rugdsl.FunctionInvocationContext<?>` | ** |

#### Operation: `moveUnder`

Move the contents of this project under the given path, preserving its present path under that

##### Parameters

| Name        | Type           | Description  |
| ------------|:---------------|:-------------|
| ***path*** | `class java.lang.String` | *The root path to move the file to* |

#### Operation: `name`

Return the name of the project. If it's in GitHub, it will be the repo name. If it's on the local filesystem it will be the directory name

##### Parameters

*None*

#### Operation: `nodeTags`

Tags attached to the node

##### Parameters

*None*

#### Operation: `nodeType`

Tags attached to the node

##### Parameters

*None*

#### Operation: `packages`

List the packages in this project

##### Parameters

*None*

#### Operation: `println`

Cause the editor to print to the console. Useful for debugging if running editors locally.

##### Parameters

| Name        | Type           | Description  |
| ------------|:---------------|:-------------|
| ***msg*** | `class java.lang.String` | *The message to be displayed* |

#### Operation: `projects`

Don't use. Merely intended to simplify the life of the Rug to TypeScript transpiler.

##### Parameters

*None*

#### Operation: `regexpReplace`

Replace all occurrences of the given regular expression in this project

##### Parameters

| Name        | Type           | Description  |
| ------------|:---------------|:-------------|
| ***regexp*** | `class java.lang.String` | *The regular expression to search for* |
| ***replacement*** | `class java.lang.String` | *The string to replace matches with* |

#### Operation: `renamePackage`

Rename the given package. All package under it will also be renamed

##### Parameters

| Name        | Type           | Description  |
| ------------|:---------------|:-------------|
| ***oldPackage*** | `class java.lang.String` | *Old package name* |
| ***newPackage*** | `class java.lang.String` | *The new package name* |

#### Operation: `replace`

Replace all occurrences of the given string literal in this project. Use with care!

##### Parameters

| Name        | Type           | Description  |
| ------------|:---------------|:-------------|
| ***literal*** | `class java.lang.String` | *The string to look for* |
| ***replaceWith*** | `class java.lang.String` | *The string to replace matches with* |

#### Operation: `replaceInPath`

Globally replace all occurrences of the given string literal in file paths in this project

##### Parameters

| Name        | Type           | Description  |
| ------------|:---------------|:-------------|
| ***literal*** | `class java.lang.String` | *The string to search for* |
| ***replacement*** | `class java.lang.String` | *The string to replace in the paths if found* |

