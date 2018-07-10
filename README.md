# Integrate OpenStreetMap with Drupal

## Setup

The setup is very straignt forward

* Clone the git repo locally

```
git clone git@github.com:shahinam/OpenStreetMap.git
```

* Switch to the cloned project.

```
cd OpenStreetMap
```

* Run the application

```
docker-compose up -d
```

Make sure `docker` and `docker-compose` are installed.

* Wait for about a minute for container to spinup and import database.

* Check the site by pointing your browser to `http://localhost:8080/`

## Implemenation details

* The application uses two Drupal modules to integrate the OSM
  - Geo Fieldgeofield
  - Leaflet

* There is a content type called `Place` with following fields
  - `Title` A text field to store place name. 
  - `Description` A long text field to store short descrption about the place.
  - `Coordinates` A geofield which stores latitude and longitute.

* A view which display a map with all the published nodes displayed.
Check the view at `http://localhost:8080/map/osm`
