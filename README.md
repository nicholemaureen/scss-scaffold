# Oomph's scss-scaffold

This is Oomph's boilerplate scaffold for starting front-end theme development.

## Team Maintenance

All UI Team Members are expected to help maintain this scaffold and update
best practices as we work on other projects. The workflow should be something
like this:

* A Team Member clones this repo and starts a new project with it.
* They notice something that they need to change in the scaffold that is
NOT specific for this project, like a default markup pattern has changed, a
browser has become unsupported, or an error or omission in a function needs
an update.
* The Team Member changes it in their new project, AND ALSO goes back to the
scaffold and files an issue in Github and assigns it to themself.
* They can then resolve the issue by making the change needed and submitting a
PR for review, or they can go back and handle the issue later.

In this way, maintenance becomes a team effort and no one person is burdened
with all maintenance responsibilities.

Likewise, if there is a new great idea that we should incorporate into this
scaffold, any Team Member can file an issue and bring the idea forward for
review and inclusion.

## Getting Started

### Add Bourbon & Neat

If you are going to compile and test this scaffold locally, you will need to
add the dependencies Bourbon and Neat:

```sh
# You already have SASS installed, right?
$ which sass

# You should see a path to your local SASS copy
# Not there? Install it:
$ sudo gem install sass

# Requires Sass 3.3+
$ sass --v
$ Sass 3.4.20

# Old version? Update!
$ sudo gem update sass

# Never installed bourbon or neat? Install their gems first.
$ sudo gem install bourbon
$ sudo gem install neat

# Then, navigate to the `libraries` directory to install:
$ cd path/to/scaffold/libraries
$ bourbon install
$ neat install
```

### Compile manually
While working on the Scaffold, compile your CSS and test the output by running
it in this folder. Here's the command:

```sh
$ sass --watch path/to/styles.scss:path/to/output.css --style compressed
```

### Linting
For our SCSS testing we are using `pre-commit` hooks provided by `git` more
info here: [pre-commit by Yelp](http://pre-commit.com/)

##### Installing Pre-Commit
If you use Homebrew, run `brew install pre-commit`
If not, freakin install it from [Homebrew](http://brew.sh/)

Currently the linter is setup to only run on changed files and only when commiting.
Occasionaly we have projects that for whatever reason need us to "tweak" these
standards and the linter process allows two simple ways to do so.

1. To notify the linter to not run on certain code blocks you can use some
special comments, read more here: [Disabling Linters via Source](https://github.com/brigade/scss-lint#disabling-linters-via-source)

2. To override the linter during the actual commiting process, you can use
the `--no-verify` flag when doing your commit. For more information review the [Advanced Features](http://pre-commit.com/#advanced) of pre-commit.

# Happy theming!
