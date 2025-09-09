# Grommet Theme HPE Codemod

A codemod project for migrating Grommet theme t-shirt size props and related values from v6 to v7.

## Features

- Automated migration of t-shirt size props (e.g., `gap`, `margin`, `pad`, `thickness`, `border`, `height`, `width`, `round`, etc.)
- Handles JS, JSX, TS, and TSX files
- Scan mode to detect t-shirt sizes without making changes
- Dry run and verbose options

## Usage

### 1. Install dependencies

```
npm install
```


### 2. Run the codemod

After publishing to npm, you can run the codemod directly with npx:

```
npx grommet-theme-hpe-codemod migrate-theme-v6-to-v7 <path> [options]
```

Or, for local development:

```
node bin/cli.js migrate-theme-v6-to-v7 <path> [options]
```

#### Options

- `--dry` Run in dry mode (no changes)
- `--scan` Scan for t-shirt sizes without transforming
- `--verbose` Set verbosity level (0, 1, or 2). Default is 0
- `--quote` Set quote style (single or double). Default is double
- `--help` Show help message

#### Example usage

```
node bin/cli.js migrate-theme-v6-to-v7 src/ --scan
node bin/cli.js migrate-theme-v6-to-v7 src/
node bin/cli.js migrate-theme-v6-to-v7 src/ --dry
node bin/cli.js migrate-theme-v6-to-v7 src/ --quote single --dry
node bin/cli.js migrate-theme-v6-to-v7 src/ --verbose 1 --dry
node bin/cli.js migrate-theme-v6-to-v7 src/ --verbose 2
```

## Adding More Transforms

Add new codemod scripts to the `transforms/` directory and register them in `bin/cli.js`.

## License

MIT
