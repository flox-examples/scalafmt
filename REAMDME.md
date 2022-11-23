usage:


Run `flox build`

the built version can now be tested

```shell
  $ result/bin/scalafmt --version
  scalafmt 3.5.2

  $ result/bin/scalafmt --help
  scalafmt 3.5.2
  Usage: scalafmt [options] [<file>...]

    -h, --help               prints this usage text
    -v, --version            print version
    <file>...                file, or directory (in which all *.scala files are to be formatted);
                             if starts with '@', refers to path listing files to be formatted
                             (with "@-" referring to standard input as a special case)
    --stdout                 write formatted files to stdout
    --exclude <value>        file or directory, when missing all *.scala files are formatted.
    --respect-project-filters
                             use project filters even when specific files to format are provided
    -c, --config <value>     a file path to .scalafmt.conf.
    --config-str <value>     configuration defined as a string
    --stdin                  read from stdin and print to stdout
    --no-stderr              don't use strerr for messages, output to stdout
    --assume-filename <value>
                             when using --stdin, use --assume-filename to hint to scalafmt that the input is an .sbt file.
    --reportError            exit with status 1 if any mis-formatted code found.
    --test                   test for mis-formatted code only, exits with status 1 on failure.
    --check                  test for mis-formatted code only, exits with status 1 on first failure.
    --diff                   Format files listed in `git diff` against master.
                             Deprecated: use --mode diff instead
    --mode <value>           Sets the files to be formatted fetching mode.
                             Options:
                                diff: format files listed in `git diff` against master
                                changed: format files listed in `git status` (latest changes against previous commit)
                                any: format any files found in current directory
                                anygit: format any git-tracked files found in current directory
    --diff-branch <value>    If set, only format edited files in git diff against provided branch. Has no effect if mode set to `changed`.
    --build-info             prints build information
    --quiet                  don't print out stuff to console.
    --debug                  print out diagnostics to console.
    --non-interactive        disable fancy progress bar, useful in ci or sbt plugin.
    --list                   list files that are different from scalafmt formatting
  Examples:
  scalafmt # Format all files in the current project, configuration is determined in this order:
           # 1. .scalafmt.conf file in current directory
           # 2. .scalafmt.conf inside root directory of current git repo
           # 3. no configuration, default style
  scalafmt --test # throw exception on mis-formatted files, won't write to files.
  scalafmt --mode diff # Format all files that were edited in git diff against master branch.
  scalafmt --mode changed # Format files listed in `git status` (latest changes against previous commit.
  scalafmt --diff-branch 2.x # same as --diff, except against branch 2.x
  scalafmt --stdin # read from stdin and print to stdout
  scalafmt --stdin --assume-filename foo.sbt < foo.sbt # required when using --stdin to format .sbt files.
  scalafmt Code1.scala A.scala       # write formatted contents to file.
  scalafmt --stdout Code.scala       # print formatted contents to stdout.
  scalafmt --exclude target          # format all files in directory excluding target
  scalafmt --config .scalafmt.conf   # read custom style from file.
  scalafmt --config-str "style=IntelliJ" # define custom style as a flag, must be quoted.
  Please file bugs to https://github.com/scalameta/scalafmt/issues
```
