# Installfest Step 3: PHP and Postgres

**Plan overview:**

1. Install PHP, a back end web development language.
2. Install PostgreSQL, a database the database we'll use with our PHP stack.
3. Install MAMP, a package that bundles together three very useful tools: Apache, MySQL, and PHP.

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
<summary>Still Having Trouble?</summary

### Homebrew PHP

The package you just installed also has its own [documentation here](https://github.com/Homebrew/homebrew-php).  If you are still seeing issues, you may want to check their site out.

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

3. Now create your first database with:

  ```bash
  createdb
  ```

4. Check that your install worked

    ```bash
    which psql
    ```
    
This should return 

    ```bash
    /usr/local/bin/psql
    ```

## MAMP

MAMP stands for:

- *M*ac Operating System
- *A*pache Web Server
- *M*ySQL dialect of SQL
- *P*HP back-end language

1. Download [MAMP](https://www.mamp.info/en/downloads/)
1. Double click the .pkg file and follow prompts
1. Double click /Applications/MAMP/MAMP
1. Point MAMP to your WDI working directory
	- Click on Preferences
	- Click on Web Server
	- Click the folder icon next to "Document Root" and find a suitable directory to work out of
		- We recommend a folder, inside your working directory, called `mamp`
	- Click OK
1. Click `Start Servers`
1. Go to <http://localhost:8888/>

If you see a page that says `Index of /`, MAMP setup is complete.

<details>
<summary>Postico (optional)</summary>
### Postico

Postico is a GUI tool to view the contents of your Postgres database. 

1. Go to <a href="https://eggerapps.at/postico/" target="_new">eggerapps.at/postico/</a> and download the free version.
2. Install it by unzipping the downloaded zip and then dragging `Postico.app` into your `Applications` directory.

</details>
