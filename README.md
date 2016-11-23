#Please be aware that this project is far from finished! 

# MapsManagementSystem
Small backend system for managing multiple pointers on a Google Maps for embedding.

The pointers are printed out to a JSON-file, which can then be parsed by the embedded Google Maps. This JSON-file can be requested by CORS to a subdirectory on the same server, or with the right permissions and tinkering, the file could be printed to another server.

____________________________________________

##Installation

####PHP-installation
 - Download the zip-file and unpack it for preperations.
 - In the index.php, insert the MYSQL database information, this includes the database server IP, username for user with the right permissions, the password for the user, and finally the name of the database.
 - Further down, the actual query to the database is specified. Be sure to select all the table rows you need.

####JavaScript-installation
 - In the "Maps_api.js" file, you will find the "roadAtlasStyles", which speciefies how your map will look when i has been embedded, documentation for this can be found [here](https://developers.google.com/maps/documentation/javascript/styling)
 - The following variable "mapOptions", a the "center" selector specifies the center of the map, THIS IS A LATLNG!
 - The "getJSON" function need to get the specific URI for which "markers.json" the embeded map needs to parse.
 - Finally the last bit of JavaScript specifies the content of a "contentBox", that appears when the pointers are clicked. This is a simple markup, echoed out so this can look just like you want it, and it can be styled from "style.css".
