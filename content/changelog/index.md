# Changelog

## 0.3.2

- Run-time bug fix for windows (by [@anuraghazra](https://github.com/anuraghazra))

## 0.3.1

- Run bug fix when content is empty (by [@Judionit](https://github.com/Judionit))
- Complete refactor and added e2e tests

## 0.3.0

- We now support plugins 🎉 Example: [https://github.com/saurabhdaware/abell-sitemap-plugin](https://github.com/saurabhdaware/abell-sitemap-plugin) (Issue [#15](https://github.com/abelljs/abell/issues/15))
- Nested folders in `content` now maintain structure (Resolved Issue [#19](https://github.com/abelljs/abell/issues/19))
- **BREAKING CHANGE** All assets should be inside `content/<slug>/assets/` folder ([#22](https://github.com/abelljs/abell/issues/22))
- Keeping dev-server alive when not defined errors occur (Patially fixes [#16](https://github.com/abelljs/abell/issues/16))
- Keeping dev-server alive when new blog added/deleted (Fixed [#23](https://github.com/abelljs/abell/issues/23))
- Refresh cache in dev-server to avoid display of old data ([#26](https://github.com/abelljs/abell/issues/26))
- Crash on `content/index.md` change fix (Issue [#21](https://github.com/abelljs/abell/issues/21))
- Removed `ignoreInDist`, will be auto-calculated depending on which files are required (Resolves [#25](https://github.com/abelljs/abell/issues/25))
- Refactoring
- Ability to change socket ports with `abell serve --socket-port 3000 --port 5000`
- **BREAKING CHANGE** `./theme/[$slug]/index.abell` changed to `./theme/[$path]/index.abell`
- Fix of nested .abell files in `theme`
- Added `$root` to global variables in all `.abell` files.
- Multiple templates (Resolved [#31](https://github.com/abelljs/abell/issues/31))

## 0.2.20

- Way to overwrite `$createdAt` and `$modifiedAt` values from `meta.json` in content. Resolved #14

## 0.2.19 [Not Released on NPM]

- Warnings are displayed in yellow color
- abell-renderer updated to 0.1.10 [Changelog of Abell Renderer](https://github.com/abelljs/abell-renderer/releases/tag/v0.1.10)

## 0.2.18

- **BUG FIX**
  Caching of files required from `.abell` files during dev-server fixed. Now Auto-refresh will work on required files as well.

## 0.2.17

- Having `content` directory is no more neccessary. Ability to build a static site which is not dependent on markdown content.

## 0.2.16

- Fix for dev-server not having right content-type of `.mjs` files.

## 0.2.15

- Having `[$slug]/index.abell` is no more neccessary.

## 0.2.14

- Prefetch now recognizes the links that are preloaded in the next page.

## 0.2.13

- Forgot to add .vscode to npmignore in last update and my vscode configs went with the package 😭😭

## 0.2.12

- Added `as=<type>` to prefetched links during build-time

## 0.2.11

- Building all `.abell` files inside `theme` folder. (Thanks to [@akash-joshi](https://github.com/akash-joshi) for PR [#12](https://github.com/abelljs/abell/pull/12))
- **BREAKING CHANGE**
  Dropping option of `templateExtension` from `abell.config.js`
- Tiny Refactor og ignoring files flow.

## 0.2.10

- **MAJOR UPDATE: Website Performance Improvements**
  All links from content's template will be prefetched on the index page.

## 0.2.9

- Secretly supporting `ignoreInBuild` option in abell configs to remove files from destination (can be used to ignore files that are only required in build time)

## 0.2.8

- **BREAKING CHANGE**
  Paths in `require` are now relative to the respective .abell files.

## v0.2.7

- **BREAKING CHANGE**
  Default sourcePath changed from `src` to `theme`
- Documentation update

## v0.2.6

**MAJOR UPDATE: Build Performance Improvements**

- `browser-sync` removed from dependency
- New faster dev server written from complete scratch.

## v0.2.5

- Migrated from `markdown-it` package to `remarkable`

## v0.2.4

- Build adds `id` to Markdown to HTML rendered content.

## v0.2.3

- **BREAKING CHANGE**
  `$contentList` changed to `$contentArray`
- Refactoring of how variables are handled internally
- `$contentObj` and `$slug` variables added
- **BREAKING CHANGE**
  `template/content.abell` changed to `[$slug]/index.abell`

## v0.2.2

- **BREAKING CHANGE**
  Syntax for importing content changed.

```js
\{{ import_content '\{{meta.$slug}}/index.md' }}
```

⬇️

```js
{
  {
    $importContent(meta.$slug + '/index.md');
  }
}
```

- Update to [abell-renderer v0.1.4](https://github.com/abelljs/abell-renderer/releases/tag/v0.1.4)

## v0.2.1

- **BREAKING CHANGE**
  Default folder to read content template changed from `[content]/index.abell` to `template/content.abell`.
- Build time reduced. (Pre-calculating directories and contentList before execution)
- More accurate Build times.
- Error handling on Build Failures.
- Documentation design updates.

## v0.2.0

Migration to [abell-renderer](https://github.com/abelljs/abell-renderer) v0.1.0

...Detailed ChangeLog at [abell-renderer v0.1.x Changelog](https://github.com/abelljs/abell-renderer/blob/main/CHANGELOG.md#v010)

## v0.1.15

Added build time to logs

## v0.1.14

- Documentations Fixes [#6](https://github.com/abelljs/abell/pull/6) (Thank you [@0xflotus](https://github.com/0xflotus))
- Fixed [#5](https://github.com/abelljs/abell/issues/5) (dev-server content going blank issue 🎉💃)

## v0.1.13

Directory listing fix for node v8 ([#3](https://github.com/abelljs/abell/pull/3) by [@Pika1998](https://github.com/Pika1998))

## v0.1.12

- A little more stable API (still not final though)
- Migration from Mustache to Abell Renderer
- Ability to write JS in HTML inside `\{{`, `}}` tags

## < v0.1.11

- Experimented stuff..
