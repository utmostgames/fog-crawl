# fog-crawl
Friend of Gamers - Crawling Around

About FOG: The dream of the open hobbyist web. A published standard for tabletop game masters in a digital age. 

FOG-Crawl is presentation software for "Fog of War" and Exploration: a javascript 'single-page-app' which accepts formatted JSON data from anywhere on the web, and utilizes browser local storage to track where your players are and have been on your map. FOG-Crawl was built to support transparent SVG, but most graphic formats your browser recognizes can be mapped.

FOG-Crawl is not a Virtual Table Top! FOG-Crawl is not networked! It is a View for the game master to Show the players as they explore.

RECOMMENDED:
Clone me to [YourOwnCampaigns].github.io: this will allow you to keep your own version and more importantly host images on the same domain and pull my upgrades. If you have your own domain, please go nuts: *I AM NOT SELLING THIS*

Digitize your map: I used GIMP to take a photograph of a hand-drawn dungeon, and turn all the impassable terrain to transparency. Then I Exported the Path as an SVG file with a stroke and fill. FOG-Crawl is designed to ALLOW player positioning on filled areas and DISALLOW it on unfilled. Currently (ver 0.5.0.1), I am not going through the hassle of using an HTML5 Canvas element, so that means all PNG and JPG files are treated as fully filled. If you have a large walkable area or are used to other VTTs, you won't know what you're missing until you try a huge SVG!
