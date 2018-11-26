# gwent-data-release

JSON produced by the script in gwent-data

## Usage

You can use the data in this repository anyway you want, as long as you make sure to conform to the [Gwent Fan Content Guidelines](https://www.playgwent.com/en/fan-content). Here are two easy ways to use the data in your project:

### A. Direct download

You can directly download the raw JSON files from GitHub and use them as you wish.

### B. NPM dependency

Alternatively you can install it as an NPM dependency in your project. Since this is not published as an NPM package, you need to install it from GitHub directly:

```
{
  "dependencies": {
    "gwent-data-release": "GwentCommunityDevelopers/gwent-data-release"
  }
}
```

This will always install the `master` version. Instead, you can specify the SHA of a commit, to avoid unexpected updates:

```
{
  "dependencies": {
    "gwent-data-release": "GwentCommunityDevelopers/gwent-data-release#039f508ee2dabe5d108dba91310a849de3185b99"
  }
}
```

Then run `npm install`. You can now import any files by path:

```js
import cards from 'gwent-data-release/cards'
```
