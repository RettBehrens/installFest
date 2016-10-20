# Installfest Step 3: PHP and Postgres

**Plan overview:**

1. Install PHP, a back end web development language.
2. Install PostgreSQL, a database the database we'll use with our PHP stack.

## PHP

### Setup

Setup the homebrew/dupes tap which has dependencies we need:

```bash
brew tap homebrew/dupes
```

Setup the homebrew/versions tap which has dependencies we need:

```bash
brew tap homebrew/versions
```

Then, run the following in your command-line:

```bash
brew tap homebrew/homebrew-php
```

### Install

Finally, install PHP version 5.6:

```bash
brew install php56
```

<details>
<summary>Still Having Trouble?</summary>
### Homebrew PHP

The package you just installed also has its own [documentation here](https://github.com/Homebrew/homebrew-php).  If you are still seeing issues, you may want to check their sit out.

</details>



## PostgreSQL 

### Postgres

1. Install postgres via Homebrew
  ```bash
  brew install postgres
  ```

2. Configure postgres to start when the system does.

  ```bash
  mkdir -p ~/Library/LaunchAgents

  ln -sfv /usr/local/opt/postgresql/*.plist ~/Library/LaunchAgents
  ```

3. Check that your install worked

    ```bash
    which psql
    ```
This should return 

    ```bash
    /usr/local/bin/psql
    ```

<details>
<summary>Postico (optional)</summary>
### Postico

Postico is a GUI tool to view the contents of your Postgres database. 

1. Go to <a href="https://eggerapps.at/postico/" target="_new">eggerapps.at/postico/</a> and download the free version.
2. Install it by unzipping the downloaded zip and then dragging `Postico.app` into your `Applications` directory.

</details>
