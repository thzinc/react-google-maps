### Map with a TrafficLayer

```jsx
const { compose, withProps } = require("recompose");
const {
  withScriptjs,
  withGoogleMap,
  GoogleMap,
  TrafficLayer,
} = require("@syncromatics/react-google-maps");

const MapWithATrafficLayer = compose(
  withProps({
    googleMapURL: GOOGLE_MAP_URL,
    loadingElement: <div style={{ height: `100%` }} />,
    containerElement: <div style={{ height: `400px` }} />,
    mapElement: <div style={{ height: `100%` }} />,
  }),
  withScriptjs,
  withGoogleMap
)(props =>
  <GoogleMap
    defaultZoom={8}
    defaultCenter={{ lat: 41.9, lng: -87.624 }}
  >
    <TrafficLayer autoUpdate />
  </GoogleMap>
);

<MapWithATrafficLayer />
```
