# fog-crawl
Friend of Gamers - Crawling Around

*About FOG: The dream of the open hobbyist web. A published standard for tabletop game masters in a digital age.*

FOG-Crawl is presentation software for "Fog of War" and Exploration: a javascript 'single-page-app' which accepts formatted JSON data and utilizes browser local storage to track where your players are and have been on your map. FOG-Crawl was built to support transparent SVG, but most graphic formats your browser recognizes can be mapped.

* FOG-Crawl is not a Virtual Table Top, but it shares many of the same features.
* FOG-Crawl is not networked, but it is online wherever you put it.
* FOG-Crawl is a View for the game master to Show the players as they explore.

# How to use:
* The base version is here https://utmostgames.github.io/ but it doesn't have YOUR maps, yet.
* Take a look at the sample _CHAR.JSON_ file, then Crawl around for a little bit *(hit 'c' to enter Character Mode and you can click around)*.
* When you see what's going on, export the _CHAR.JSON_ file and supply the image paths and character names for your party. Import, test it out.
* Import your map. Size it. Center it. Skip the regions til you have a list of images and descriptions ready.
* That's it, really. There are a few key commands while you Crawl. Better documentation on that is incoming. *(Hit 't' in character mode and click down the hallway!)*


## RECOMMENDED:

* __Clone me to [YourOwnCampaigns].github.io:__ this will allow you to keep your own version and more importantly host images on the same domain and pull my upgrades. If you have your own domain, please go for it. FOG-Crawl works best with map images on the same domain!

* __Digitize your map:__ I used GIMP and a photograph of a hand-drawn dungeon, and turned all the impassable terrain to transparency. Then I Exported the Path as an SVG file with a stroke and fill. FOG-Crawl is designed to ALLOW player positioning on filled areas and DISALLOW it on unfilled. *It takes a lot of RAM to use an HTML5 Canvas element just for detecting transparent pixels, so that means all PNG and JPG files are treated as fully filled. If you have a large walkable area such as outdoors, or are used to other VTTs, you won't know what you're missing until you try a huge SVG!*

* __Host your campaign map on the same domain as your copy of FOG-Crawl:__ the aforementioned [YourOwnCampaigns].github.io, or anywhere else you host this javascript and html. Unfortunately, almost every image host you can use has Cross-Origin Resource Security policies in place. This means that even if you Digitized Your Map to a cool SVG as above, you have to host it on an 'opened' domain, and I didn't find any, and I couldn't get any proxies to work. The workaround is Same-Origin for your SVG. Just upload _your_map.svg_ to your github.io and path to it in the config!

* __Speaking of the config:__ there are TWO json files: _CHAR.JSON_ for characters and _CONFIG.JSON_ for everything else. Cross-Origin again, but you can paste into the application, or just host your JSON on your github.io!

*FOG-Crawl is very alpha right now. I threw it together and got it stable enough to solicit feature suggestions. So contribute additional functionality you'd like to see; but please remember the idea here is that with an exported campaign JSON, this is a stateless application.*

# FOG The Requests for Comment:

### FOG 1 - Character Tokens: a schema for top-down characer tokens
```
{
    "name":STRING,      // Display name of character
    "src":URI,          // URI of image file for top-down token
    "face":STRING,      // Optional; cardinal direction, capitalized, of the facing of the image file in above URI. Default is "N" for "north/upward"
    "square":INT,       // Optional; pixel size of the image file in above URI. Default is 20 pixels value
    "special":[STRING]  // Optional; string array of lowercase Keywords for functional changes. Ex: "infra" changes default lighting color for character
}
```
