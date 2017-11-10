# iPhone X Availability Node CLI

A node cli tool I put together to check the iPhone X in-store availability near me instead of having to refresh the apple website over and over again.

**Warning**: This was very quickly put together so it is very rough and has a lot of room for improvement. It did end up being successful in letting me know there was some new stock near me a few hours after I built it so at the very least: it works!

Feel free to submit a pull request with improvements or just simply fork it and modify it for your own needs. Soon there won't be a shortage of iPhones anymore so this tool will be irrelevant.

### How to use

1. Clone this repository
1. Instal dependencies by running `npm install`
1. Run the program by running `node index.js --zip=12345`

### Examples

Check availability for TMOBILE iPhone X 256gb in space gray every 30 seconds near the zip code 12345 (pretty much the default settings so we don't need to specify them here, the zip code is always required though)
```
node index.js --zip=012345
```

Check availability for ATT iPhone X 64gb in silver every minute near the zip code 02115
```
node index.js --carrier=ATT --color=silver --storage=64 --delay=60 --zip=02115
```

### Options
| option  | accepted values                               | default                               |
| ------- | --------------------------------------------- | ------------------------------------- |
| carrier | `'ATT'`, `'SPRINT'`, `'TMOBILE'`, `'VERIZON'` | `'TMOBILE'`                           |
| model   | `'x'`                                         | `'x'`                                 |
| color   | `'silver'`, `'gray'`                          | `'gray'`                              |
| storage | `64`, `256`                                   | `256`                                 |
| delay   | Integer number of seconds between requests    | `30`                                  |
| zip*    | 5 digit US zip code                           | Not provided, you must enter your own |

*\*required*
