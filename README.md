# gwent-data-release

JSON produced by the script in gwent-data.

## How long does it take this repo to get updated after a Gwent update?

It usually takes a couple of days after a Gwent update for this repo to be updated. Card data can be collected from the game files immediately, however it takes a couple of days for CDPR to send over the card images and then for them to be uploaded to the Google Cloud Storage bucket.

The script that generates this data is open source. If you need data quicker than this repo updates, then you can generate it yourself using the script in [gwent-data](https://github.com/GwentCommunityDevelopers/gwent-data).

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
