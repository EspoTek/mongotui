# Mongotui

<p>
    <a href="https://github.com/kreulenk/mongotui/releases"><img src="https://img.shields.io/github/release/kreulenk/mongotui.svg" alt="Latest Release"></a>
    <a href="https://goreportcard.com/report/github.com/kreulenk/mongotui"><img src="https://goreportcard.com/badge/github.com/kreulenk/mongotui"></a>
</p>

Mongotui is a terminal user interface MongoDB client that is designed to be easy to use and fast.

![demo.gif](./docs/demo/demo.gif)

## Usage
Mongotui aims to make switching from mongosh easy as it has similar flags and commands when first connecting
to a MongoDB server.

If you have a local MongoDB server running on the default port and no authentication, you can run the following command to get up and running.
```bash
mongotui localhost
```

Mongotui also accepts full MongoDB connection strings.

```bash
mongotui mongodb://user:password@localhost:27017
```


Explore the help menu if additional connection information is required.
```bash
mongotui --help
```


## Features
- Similar connection flags/options to mongosh
- Navigate between databases/collections/documents
- Filter displayed databases/collections
- Query for specific documents
- Pagination of document results
- View an entire document
- Insert a new database/collection/document
- Edit a document using your `$EDITOR` of choice
- Drop databases/collections and delete documents

## Installation

### macOS & Linux (latest build of this fork)

Every push to `main` is built for macOS and Linux (amd64 and arm64) by GitHub Actions and published
to the rolling `latest` release. To download and install the right binary for your machine:

```bash
curl -fsSL "https://github.com/EspoTek/mongotui/releases/latest/download/mongotui-$(uname -s | tr '[:upper:]' '[:lower:]')-$(uname -m | sed -e 's/x86_64/amd64/' -e 's/aarch64/arm64/').tar.gz" | tar -xz
sudo mv ./mongotui /usr/local/bin/mongotui
```

### Homebrew (upstream release)

The upstream project publishes to a Homebrew tap. Note that this installs kreulenk's release,
which does not include this fork's changes.

```bash
brew tap kreulenk/brew
brew install mongotui
```

### Build From Source

Ensure that you have at least Go 1.24.5 installed on your system.

Then, run
```bash
make install
```
