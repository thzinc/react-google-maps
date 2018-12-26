### Map with a BicyclingLayer

```jsx
const { compose, withProps } = require("recompose");
const {
  withScriptjs,
  withGoogleMap,
  GoogleMap,
  BicyclingLayer,
} = require("react-google-maps");

const MapWithABicyclingLayer = compose(
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
    defaultZoom={12}
    defaultCenter={{ lat: 34.17223, lng: -118.37897 }}
  >
    <BicyclingLayer autoUpdate />
  </GoogleMap>
);

<MapWithABicyclingLayer />
```
