# map-marker-project
Interactive map of the earthquakes.
This project was developed as a part of an online course of Object Oriented Programming in Java "https://www.coursera.org/learn/object-oriented-java/home/welcome"



 • The method checkEarthquakesForClick() has been updated to create an SimplePolygonMarker when the marker is selected by click of the mouse. SimplePolygonMarker contains all the location around the earthquake epicentre i.e all the locations on the threat circle edge. These locations collected every 1 degree out of 360 degrees by using GeoUtils.getDestinationLocation() method, which gives SimplePolygonMarker a elliptical shape. Then the marker added to a map.
 
•  The method unhideMarkers() has been update to unhide all the earthquake markers and hide the SimplePolygonMarker that represents the treat circle of the lastClicked marker.The method goes through all the map markers by using for loop and  map.getMarkers() and checks their type. If the SimplePolygonMarker is found then it is setHidden(true) otherwise the marker is found is a city or the earthquake marker that are setHidden(false).
  
•  These type of implementation saves the memory space and time for a program execution as only one marker SimplePolygonMarker at a time is created. It takes enormous amount of space and time to create SimplePolygonMarker for each earthquake marker and store those in an array. Therefore this implementation saves up unnecessary executions. 

 • Every earthquake marker have an interactive threat area, that displayed when the  earthquake marker is chosen and disappears when you click at different location on the map or choose another marker . This threat circle is tided to a map and accurately shows the exact locations that have been affected by the earthquake. Therefore it has  fixed position on the map, and doesn't saves its shape when you zoom in and out the map like other markers do.
City marker has been changed to visually represent cities in well known format, e.g Google maps.
