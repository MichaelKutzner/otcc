# Open Transport Community Conference
This is the source code for the Open Transport Community Conference website, https://open-transport.org.

The site is statically generated, using [Zola](https://www.getzola.org/), a [static site generator](https://jamstack.org/generators/).
It's design is based on [tabi](https://github.com/welpo/tabi), an accessible [theme](https://www.getzola.org/themes/), that provides many useful features.
Both were chosen to allow everyone to contribute easily.

## Contribution
As the conference will be a community event, participation and improvements are highly appreciated.
This section will describe how to set up the local repository.

### Requirement
* Git
* an editor
* Zola (see next subsection)

### Setup Zola
Zola can be downloaded as a precompiled binary from is [release page](https://github.com/getzola/zola/releases).
For further installation methods see https://www.getzola.org/documentation/getting-started/installation/.

Make sure the binary is executable.
Extract if necessary.
The following code assumes it has been added to your `PATH`.

### Prepare repository
Clone the repository and initialize the submodules.

```sh
git clone https://github.com/MichaelKutzner/otcc
cd open-transport-community-conference
git submodule update --init --recursive
```

### Test the site
Start the Zola server.

```sh
zola serve
```

The process will track changes and rebuild the site if necessary.

To build the static site files run `zola build` instead.
This will create the `public/` directory, which can be served by your webserver.

### Contribute
Please open a Pull Request for updates and improvements.
Make sure all texts are available in English.
Pages, that are not translated, should be made available by providing a symbolic link pointing to the English page, e.g.:

```sh
ln -s _index.md content/_index.de.md
```

## Troubleshooting

### The page is not rendered probably during local development
Change `base_url` in `config.toml` to match your local address, e.g.

```
base_url = "http://localhost:1111"
```
