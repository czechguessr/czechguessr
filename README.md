# CzechGuessr
Free and open-source GeoGuessr for Czechia

## Play
The fastest way:
* open `czechguessr.github.io`
* click `Play in your browser`
* in the first field enter:
    - if you want the default map: `/official-maps`
    - else follow chapter `Creating your own maps`
* select the map in the second field
* click `Play`
* now you play a few rounds
* when you want to end the game, click on the `X` in the top right corner
    - this action will also trigger itself when all the locations are used

## Creating your own maps
For creating your own maps, I recommend to use the official [SDK](https://czechguessr.github.io/czechguessr-sdk). You can also edit the JSON files yourself.
* create a map in the SDK or create the JSON file on your own
* create a folder on your computer
* create a file and copy the JSON from the SDK or your text editor (should have the `.json` ext)
* create a `CzechGuessr.json` file in the folder
* copy this code in it:
```jsonc
{
    "version": "1.0",
    "maps": [
        // filename of the json file
    ]
}
```
* start a basic HTTP server in the folder
* on `czechguessr.github.io/play` enter the path to the `CzechGuessr.json` file without the filename (not trough `file:///` but your server) and play
    - if it says `Not found`, you have a issue with `CORS`, change some settings in your HTTP server and it should work

## `npm` requirements for building on your own
```
@types/leaflet
@types/jquery
```
and `https://github.com/chriskorinek/mapy-api-ts-types`, but you need to change one method:
* change:
```typescript
getBest(coords: SMap.Coords, radius?: number, attribute?: object): void;
```
* in `class SMap.Pano` to:
```typescript
static async getBest(coords: SMap.Coords, radius?: number, attribute?: object): Promise;
```
