### Map with Ground Overlay

```jsx
const { compose } = require("recompose");
const {
  withScriptjs,
  withGoogleMap,
  GoogleMap,
  GroundOverlay,
} = require("@syncromatics/react-google-maps");

const MapWithGroundOverlay = compose(
  withScriptjs,
  withGoogleMap
)(props =>
  <GoogleMap
    defaultZoom={12}
    defaultCenter={{lat: 40.740, lng: -74.18}}
  >
    <GroundOverlay
      defaultUrl="https://www.lib.utexas.edu/maps/historical/newark_nj_1922.jpg"
      defaultBounds={new google.maps.LatLngBounds(
        new google.maps.LatLng(40.712216, -74.22655),
        new google.maps.LatLng(40.773941, -74.12544)
      )}
      defaultOpacity={.5}
    />
  </GoogleMap>
);

<MapWithGroundOverlay
  googleMapURL={GOOGLE_MAP_URL}
  loadingElement={<div style={{ height: `100%` }} />}
  containerElement={<div style={{ height: `400px` }} />}
  mapElement={<div style={{ height: `100%` }} />}
/>
```
