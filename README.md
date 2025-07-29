# Tailwind CSS with no node.js (tailwind-cli)

We will use Tailwind CSS without Node.js by using the `tailwindcss` CLI tool directly.

## Download Tailwind CSS CLI

You can download the latest version of the Tailwind CSS CLI tool from the [Tailwind CSS GitHub releases page](https://github.com/tailwindlabs/tailwindcss/releases).

For example, you can download the `tailwindcss` binary for Linux or macOS:

```bash
curl -L https://github.com/tailwindlabs/tailwindcss/releases/download/v4.1.11/tailwindcss-linux-x64 -o tailwindcss
chmod +x tailwindcss
```

## Execute Tailwind CSS CLI

For production builds, you can use the `-i` flag to specify your input CSS file and the `-o` flag to specify your output CSS file. You can also use the `--minify` flag to minify the output CSS:

```bash
./tailwindcss -i ./theme/mu-theme.css -o ./public/css/tailwind-mu.min.css --minify
```

To create both minified and unminified versions in a single command, you can chain the commands:

```bash
./tailwindcss -i ./theme/mu-theme.css -o ./public/css/tailwind-mu.css && ./tailwindcss -i ./theme/mu-theme.css -o ./public/css/tailwind-mu.min.css --minify
```

For development, you can use the `--watch` flag to automatically rebuild your CSS when you make changes to your input file:

```bash
./tailwindcss -i ./theme/mu-theme.css -o ./public/css/tailwind-mu.css --watch
```

> [WARNING] If you are using the `--watch` flag, make sure you have `watchman` installed in your system to avoid issues with file watching.