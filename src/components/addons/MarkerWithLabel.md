### Map with a MarkerWithLabel

```jsx
const { compose } = require("recompose");
const {
  withScriptjs,
  withGoogleMap,
  GoogleMap,
} = require("@syncromatics/react-google-maps");
const { MarkerWithLabel } = require("@syncromatics/react-google-maps/lib/components/addons/MarkerWithLabel");

const MapWithAMarkerWithLabel = compose(
  withScriptjs,
  withGoogleMap
)(props =>
  <GoogleMap
    defaultZoom={8}
    defaultCenter={{ lat: -34.397, lng: 150.644 }}
  >
    <MarkerWithLabel
      position={{ lat: -34.397, lng: 150.644 }}
      labelAnchor={new google.maps.Point(0, 0)}
      labelStyle={{backgroundColor: "yellow", fontSize: "32px", padding: "16px"}}
    >
      <div>Hello There!</div>
    </MarkerWithLabel>
  </GoogleMap>
);

<MapWithAMarkerWithLabel
  googleMapURL={GOOGLE_MAP_URL}
  loadingElement={<div style={{ height: `100%` }} />}
  containerElement={<div style={{ height: `400px` }} />}
  mapElement={<div style={{ height: `100%` }} />}
/>
```
