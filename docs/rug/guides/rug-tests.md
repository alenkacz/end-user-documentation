Rug provides a testing framework based on [BDD](https://en.wikipedia.org/wiki/Behavior-driven_development) concepts.

This takes the form of a test DSL that reuses features and types from Rug to ensure it is easy for Rug authors to adopt.

!!! note
    Rug is designed to support Test Driven Development using the BDD style, and 
    we've seen the greatest productivity in its early use from those that create 
    test scenarios and then follow the `red` -> `green` -> `refactor` approach.

## A Quick Overview of a Rug Test

Before taking a deeper dive into the all the syntax of Rug tests, let's look at some examples.

Using the editor defined in the [Rug Editor][rugedit] section, we want to test 
that the editor works as intended:

[rugedit]: /rug/guides/rug-editors.md#parameterize-your-editor

<!--TBD How do we display this with line numbers? Or even better can we link to this sample as a Koan and embed the code from there? -->

```rug
scenario Content should be appended to myfile.txt

let someContent = " there"

given
   myfile.txt = "Hello"

when
   AppendToFile to_append=someContent

then
  fileCount = 1
  and fileContains "myfile.txt" "Hello there"
```

Walking through this test:

* Every test starts with the keyword `scenario` followed by a free text 
  description whose only limitation is that it must not contain a `#` character, 
  otherwise any text after the `#` will be treated as a comment
* Every test is then typically broken down into three blocks of `given`, `when`, 
  `then`, following the BDD style. a `given` and `then` blocks are mandatory,
  but the `when` block is not (you could execute when-related code as part of 
  the `given` block), however for readability it is a best-practice to use 
  the `when`
* This example only has one test scenario, but it is quite common to have more 
  than one scenario in one file

Rug test scenarios are written in `.rt` files (`.rt` naturally stands for Rug 
Test) and are located within a [Rug project](/rug/reference/rug-project.md) in 
the `.atomist/tests` directory.

!!! note
    `#` is one comment approach in Rug. You can also use C-style `/* */` 
    multi-line comments as well.


## Diving into the `Given` Block Syntax

The `given` block specifies the input to the editor-under-test in the form of 
multiple *file specifications*. There are several choices for expressing file 
specs:

|  File spec |  Sample | Meaning
|---|---|---|---|
| inline file | `dir/foo.txt = "bar"` | Populates the file |
loaded file | `dir/foo.txt from "/some/path/file.txt"` | Load the file content from the archive.
| archive root | `ArchiveRoot` | Loads all the files in the archive this editor is in, excluding the content of the `.atomist` directory. This is useful and convenient when building templates, as it enables verification that the contents of the template are a valid starting point for the editor being tested.

## `When` You Run Your tests

The `when` block is optional, but for clarity helps the test consumer to 
understand where the actual test is being run. Typically this is where the 
actual editor itself is invoked.

## `Then` Assertions

The `then` block then consists of one or more assertions about the final state 
of the project.

### Some `Well-Known` Assertions

Certain well-known assertions can be used alone. These are indicated in the 
following keywords:

* `NoChange`: The scenario passes if the editor does not change the input
* `NotApplicable`: The scenario passes if the editor is not applied due to a 
  precondition not being met
* `ShouldFail`: The scenario passes if the editor fails.
* `MissingParameters`: The scenario passes if the editor fails due to missing
  parameters. Used to test parameter validation
* `InvalidParameters`: The scenario passes if the editor fails due to invalid
  parameters. Used to test parameter validation

## The Rug Test Grammar

The full grammar of Rug tests is defined as:

```
<test> ::= <given> <run> <when> <then>

<given> ::= <filespec> { <filespec> }

<filespec> ::= <filename> = <filecontents>

<when> ::= <editorname> <namedargs>

<namedargs> :: = <namedarg> { namedarg }

<namedarg> :: <argname> = <argvalue>

<then> ::= <assertion> { <assertion> }

<assertion> ::= <function> <arg>

```

## Advanced Usage

### No Change

When there's no change

```rug
scenario Foobar

given
   "src/main/java/Squirrel" = "class Squirrel {}"

when
 Rename old_class="Dog", new_class = "Cat"

then
  NoChange
```

This scenario will pass only if there's no change in the input artifact source.

### More debug information

For help debugging a failing test, set debug=true to get a little tree of the 
directory structure after the editor runs.

```rug
scenario Foobar

debug=true

given...
```

To see the contents of a file in the output, use `dump <filename>` as an 
assertion predicate, like

```rug
then
  dump outputFile
	and fileContains outputFile "should be in there"
```

For more on debugging rugs, there's a walkthrough on [The Composition](https://medium.com/the-composition/dumping-your-rug-with-rug-tests-7ec191aa713e#.ccndpk66i).
