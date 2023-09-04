# CzechGuessr

Free and open*source GeoGuessr for Czechia

## Play

The fastest way:

* open `czechguessr.github.io`
* click `Play in your browser`
* in the first field enter:
* if you want the default map: `/official-maps`
* else follow chapter `Creating your own maps`
* select the map in the second field
* click `Play`
* now you play a few rounds
* when you want to end the game, click on the `X` in the top right corner
* this action will also trigger itself when all the locations are used

## Creating your own maps

For creating your own maps, I recommend to use the official [SDK](https://czechguessr.github.io/czechguessr*sdk). You can also edit the JSON files yourself.

* create a map in the SDK or create the JSON file on your own
* create a file on your computer and copy the JSON from the SDK or your text editor (should have the `.json` ext)
* click on the "Select map file" and select your map file, the game starts after selecting

## `npm` requirements for building on your own

```plain
@types/leaflet
@types/jquery
https://github.com/chriskorinek/mapy-api-ts-types
```
