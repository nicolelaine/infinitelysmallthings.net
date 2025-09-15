# infinitelysmallthings.net

This is the source code for [infinitelysmallthings.net](https://www.infinitelysmallthings.net), a website built with [Hugo](https://gohugo.io/) and the [Blowfish theme](https://github.com/nunocoracao/blowfish), using Hugo Modules and deployed via GitHub Actions to GitHub Pages.

## Local Development

Make sure you have [Hugo Extended](https://gohugo.io/getting-started/installing/) installed.

This site is built with Hugo version:

```bash
hugo v0.150.0+extended+withdeploy darwin/arm64 BuildDate=2025-09-08T13:01:12Z VendorInfo=brew
```

To preview the site locally:

### Clone the repo
```bash
git clone https://github.com/nicolelaine/infinitelysmallthings.net.git
cd infinitelysmallthings.net
```

### Fetch Hugo module dependencies
```bash
hugo mod tidy
```

### Start the local server
```bash
./serve.sh
```

### Or manually run 
```bash
hugo server --baseURL http://localhost:1313/
```

## Deployment 

This site is automatically deployed to GitHub Pages using a GitHub Actions workflow.

Deployment steps:

Push to the main branch.

GitHub Actions runs hugo and deploys the output in the /public/ folder to the gh-pages branch.

The live site is available at:
https://www.infinitelysmallthings.net

# Repository Structure

| Folder/File          | Description                                               |
| -------------------- | --------------------------------------------------------- |
| `config/_default/`   | Hugo site configuration files (`config.toml`, etc.)       |
| `content/`           | Website's markdown content                                |
| `layouts/`           | Custom templates and overrides                            |
| `static/`            | Static assets (files, etc)                                |
| `assets/`            | Processed assets                                          |
| `archetypes/`        | Contains content templates for new pages or posts         |
| `serve.sh`           | Helper script to run the site locally                     |
| `i18n/`              | Stores translation strings for interface text             |
| `CNAME`              | Stores the custom domain                                  |
| `.gitignore`         | Everything not pushed to Git/Github                       |
| `go.mod`, `go.sum`   | Hugo Modules configuration                                |
| `.github/workflows/` | GitHub Actions deployment setup                           |

# Housekeeping

The public/ and resources folders are not committed — they are regenerated automatically.
Unused folders like data/ and themes/ were removed for clarity.

# Credits

Theme: Blowfish by @nunocoracao 
Built with Hugo
