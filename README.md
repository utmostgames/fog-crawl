# fog-crawl
Friend of Gamers - Crawling Around

*About FOG: The dream of the open hobbyist web. A published standard for tabletop game masters in a digital age.*

FOG-Crawl is presentation software for "Fog of War" and Exploration: a javascript 'single-page-app' which accepts formatted JSON data and utilizes browser local storage to track where your players are and have been on your map. FOG-Crawl was built to support transparent SVG, but most graphic formats your browser recognizes can be mapped.

FOG-Crawl is not a Virtual Table Top! FOG-Crawl is not networked! It is a View for the game master to Show the players as they explore.

RECOMMENDED:

* Clone me to [YourOwnCampaigns].github.io: this will allow you to keep your own version and more importantly host images on the same domain and pull my upgrades. If you have your own domain, please go for it. FOG-Crawl works best with map images on the same domain!

* Digitize your map: I used GIMP and a photograph of a hand-drawn dungeon, and turned all the impassable terrain to transparency. Then I Exported the Path as an SVG file with a stroke and fill. FOG-Crawl is designed to ALLOW player positioning on filled areas and DISALLOW it on unfilled. *It is an enourmous hassle and RAM usage to use an HTML5 Canvas element, so that means all PNG and JPG files are treated as fully filled. If you have a large walkable area such as outdoors, or are used to other VTTs, you won't know what you're missing until you try a huge SVG!*

* Host your campaign map on the same domain as your copy of FOG-Crawl: the aforementioned [YourOwnCampaigns].github.io, or anywhere else you host this javascript and html. Unfortunately, almost every image host you can use has Cross-Origin Resource Security policies in place. This means that even if you Digitized Your Map to a cool SVG as above, you have to host it on an 'opened' domain, and I didn't find any. The workaround is Same-Origin for your SVG. Just upload it to your github.io and path to it in the config!

* Speaking of the config: there are TWO json files: CHAR.JSON for characters and CONFIG.JSON for everything else. Cross-Origin again, but you can paste into the application, or just host your JSON on your github.io!

# How to use:
* The base version is here https://utmostgames.github.io/ but it doesn't have YOUR maps.
* Take a look at the sample CHAR.JSON file, then Crawl around for a little bit *(hit 'c' to enter Character Mode and you can click around)*.
* When you see what's going on, export the CHAR.JSON file and supply the image paths and character names for your party. Import, test it out.
* Import your map. Size it. Center it.
* That's it, really. There are a few key commands. Better documentation on that is incoming. *(Hit 't' in character mode and click down the hallway!)*

*FOG-Crawl is very alpha right now. I threw it together and got it stable enough to solicit feature suggestions. So contribute additional functionality you'd like to see; but please remember the idea here is that with an exported campaign JSON, this is a stateless application.*
