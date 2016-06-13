# Changelog

All notable changes to this project will be documented in this file. This change log follows the conventions of [keepachangelog.com](http://keepachangelog.com).

## [Unreleased]
### Additions
* Enabled Emacs' next error function to go to next Kibit suggestion. See the updated code in the README for the change.

## [0.1.5] / 2016-06-13
* Removed `(not (empty? x))` to `(seq x)` rule as they are not equivalent.
* Removed threading rules (`(-> x f)` and `(->> x f)` are fine).

## [0.1.2] / 2015-04-21
### Additions
* Clojurescript/Cljx support (cljc support coming soon). This just works™, kibit will pick up your source paths from your `project.clj`'s `:source-paths`, `[:cljsbuild :builds]`, and `[:cljx :builds]`.
* Non-zero exit codes. Kibit now exits non-zero when one or more suggestions are made. This is particularly useful for those running checks in a CI environment.
* You can now run kibit on any Clojure project without a project.clj file. Just call `lein kibit` with any number of files and folders and it will inspect the Clojure files contained within.
