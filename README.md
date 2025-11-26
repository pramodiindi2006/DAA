<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>City Planner</title>
    <!-- Include Leaflet.js CSS -->
    <link rel="stylesheet" href="https://unpkg.com/leaflet/dist/leaflet.css" />
    <!-- Include Leaflet Draw CSS for drawing controls -->
    <link rel="stylesheet" href="https://unpkg.com/leaflet-draw/dist/leaflet.draw.css" />
    <style>
        /* Set default styling for the page */
        body {
            margin: 0;
            padding: 0;
            font-family: Arial, sans-serif;
        }

        /* Full screen map */
        #map {
            width: 100%;
            height: 100vh;
        }

        /* Style for drawing tool buttons */
        .leaflet-draw-toolbar {
            z-index: 1000;
        }
    </style>
</head>
<body>

    <div id="map"></div>

    <!-- Include Leaflet.js and other necessary libraries -->
    <script src="https://unpkg.com/leaflet/dist/leaflet.js"></script>
    <script src="https://unpkg.com/leaflet-draw/dist/leaflet.draw.js"></script>

    <script>
        // Initialize the map
        var map = L.map('map').setView([28.7041, 77.1025], 12); // Default center: Delhi (latitude, longitude)

        // Add the base map layer (using OpenStreetMap)
        L.tileLayer('https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png', {
            attribution: '&copy; <a href="https://www.openstreetmap.org/copyright">OpenStreetMap</a> contributors'
        }).addTo(map);

        // Add a drawing control to allow users to draw on the map (zones, roads, etc.)
        var drawnItems = new L.FeatureGroup();
        map.addLayer(drawnItems);

        var drawControl = new L.Control.Draw({
            edit: {
                featureGroup: drawnItems
            },
            draw: {
                polygon: true,
                polyline: true,
                rectangle: true,
                circle: true
            }
        });

        map.addControl(drawControl);

        // Event listener for when a user finishes drawing a shape
        map.on('draw:created', function (event) {
            var layer = event.layer;
            drawnItems.addLayer(layer);

            // Optionally: You can save the drawn layer's data as GeoJSON
            var geojson = layer.toGeoJSON();
            console.log(geojson); // You can send this data to a backend or save it locally
        });

        // Function to create a sample zone layer (to simulate existing zones)
        var residentialZone = L.polygon([
            [28.7045, 77.1030],
            [28.7055, 77.1050],
            [28.7050, 77.1070]
        ], {color: 'green', fillColor: '#8FBC8F', fillOpacity: 0.5}).addTo(map);

        residentialZone.bindPopup("Residential Zone");

        var commercialZone = L.polygon([
            [28.7065, 77.1010],
            [28.7075, 77.1030],
            [28.7070, 77.1050]
        ], {color: 'blue', fillColor: '#87CEEB', fillOpacity: 0.5}).addTo(map);

        commercialZone.bindPopup("Commercial Zone");

        // Add event listener for the draw tool's delete button (if you want to allow shape deletion)
        map.on('draw:deleted', function (event) {
            console.log("Deleted shapes:", event.layers);
        });

        // Toggle between layers (e.g., zones)
        function toggleLayer(layer, visibility) {
            if (visibility) {
                map.addLayer(layer);
            } else {
                map.removeLayer(layer);
            }
        }

        // For example, you could toggle the residential/commercial layers by calling the function like this:
        // toggleLayer(residentialZone, false); // This will hide the residential zone.
    </script>

</body>
</html>
