### Props

* googleMapURL: String
* loadingElement: ReactElement

### Usage

```jsx static
import {
  withScriptjs,
  withGoogleMap,
  GoogleMap,
  Marker,
} from "@syncromatics/react-google-maps";

const MapWithAMarker = withScriptjs(withGoogleMap(props =>
  <GoogleMap
    defaultZoom={8}
    defaultCenter={{ lat: -34.397, lng: 150.644 }}
  >
    <Marker
      position={{ lat: -34.397, lng: 150.644 }}
    />
  </GoogleMap>
));

<MapWithAMarker
  googleMapURL={GOOGLE_MAP_URL}
  loadingElement={<div style={{ height: `100%` }} />}
  containerElement={<div style={{ height: `400px` }} />}
  mapElement={<div style={{ height: `100%` }} />}
/>
```
