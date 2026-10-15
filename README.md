# Host HTML File CLI

site: [hosthtmlfile.com](https://hosthtmlfile.com)

Log in once from your terminal:

```bash
npx host-html-file login
```

Publish a local HTML file or static project directory:

```bash
npx host-html-file publish ./dist
```

Update an existing preview link in place:

```bash
npx host-html-file update ./dist --replace https://preview.hosthtmlfile.com/abc123/index.html
```

Publish to a custom Lanvo subdomain (requires a paid plan or free trial):

```bash
npx host-html-file publish ./dist --domain myapp.lanvo.app
```

If the subdomain is already linked to a project you own, the project is updated in place. Otherwise a new project is published and the subdomain is bound to it.

Install the skill from the npm package contents:

```bash
npx host-html-file install
```

By default this installs to Codex:

```text
~/.codex/skills/host-html-file
```

You can choose an agent explicitly:

```bash
npx host-html-file install --agent codex
npx host-html-file install --agent claude
npx host-html-file install --agent cursor
npx host-html-file install --agent all
```

The package ships the skill source files directly. It does not download a skill zip during installation.
Login sessions are stored at `~/.host-html-file/config.json`. An existing session at `~/.htmlshare/config.json` is still read until the next login writes the new file.
