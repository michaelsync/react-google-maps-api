# HeatmapLayer example

```jsx
const { GoogleMap, LoadScript, HeatmapLayer } = require("../../");
const ScriptLoaded = require("../../docs/ScriptLoaded").default;

<ScriptLoaded>
{() => 
  <GoogleMap
    // optional
    id="heatmap-layer-example"
    // required to set height and width either through mapContainerClassName, either through mapContainerStyle prop
    mapContainerStyle={{
      height: "400px",
      width: "800px"
    }}
    // required
    zoom={13}
    // required
    center={{
      lat: 37.774546,
      lng: -122.433523
    }}
  >
    <HeatmapLayer
      // optional
      onLoad={heatmapLayer => {
        console.log('HeatmapLayer onLoad heatmapLayer: ', heatmapLayer)
      }}
      // optional
      onUnmount={heatmapLayer => {
        console.log('HeatmapLayer onUnmount heatmapLayer: ', heatmapLayer)
      }}
      // required
      data={[
  new google.maps.LatLng(37.782, -122.447),
  new google.maps.LatLng(37.782, -122.445),
  new google.maps.LatLng(37.782, -122.443),
  new google.maps.LatLng(37.782, -122.441),
  new google.maps.LatLng(37.782, -122.439),
  new google.maps.LatLng(37.782, -122.437),
  new google.maps.LatLng(37.782, -122.435),
  new google.maps.LatLng(37.785, -122.447),
  new google.maps.LatLng(37.785, -122.445),
  new google.maps.LatLng(37.785, -122.443),
  new google.maps.LatLng(37.785, -122.441),
  new google.maps.LatLng(37.785, -122.439),
  new google.maps.LatLng(37.785, -122.437),
  new google.maps.LatLng(37.785, -122.435)
]}
    />
  </GoogleMap>
}
  </ScriptLoaded>
```
