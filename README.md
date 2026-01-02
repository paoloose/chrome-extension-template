# My setup for Chrome extensions

A simple and modern setup for writing chrome extensions (manifest v3) with TypeScript and Bun

## How to use

This extension is designed with two parts:

- The injector (`injection.js`), which is registered as a content script, and
  loaded in a selected group of pages (or any)

- The actual codebase, whose entrypoint is located in `src/main.ts`

Because the code is written in TypeScript, a compile and bundle state must be
done before testing/publishing your code

```console
bun run build.ts
```

## How to test

Go to `chrome://extensions`, enable the Developer Mode switch, and click
"Load unpacked"

![Extensions menu](assets/unrelated/extensions_site.png)

Select the directory where this project is located, and that's it.

Verify that the script being injected correctly. When testing new changes,
make sure you rebuild the code and reload the extension

![Reload button](assets/unrelated/extension_reload.png)

## Useful links

- Manifest v3 specification <https://developer.chrome.com/docs/extensions/reference/manifest>
- Permissions <https://developer.chrome.com/docs/extensions/reference/api/permissions>
