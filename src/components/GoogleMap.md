### Map with controlled zoom

```js
const { compose, withProps, withState, withHandlers } = require("recompose");
const FaAnchor = require("react-icons/lib/fa/anchor");
const {
  withScriptjs,
  withGoogleMap,
  GoogleMap,
  Marker,
  InfoWindow,
} = require("@syncromatics/react-google-maps");

const MapWithControlledZoom = compose(
  withProps({
    googleMapURL: GOOGLE_MAP_URL,
    loadingElement: <div style={{ height: `100%` }} />,
    containerElement: <div style={{ height: `400px` }} />,
    mapElement: <div style={{ height: `100%` }} />,
  }),
  withState('zoom', 'onZoomChange', 8),
  withHandlers(() => {
    const refs = {
      map: undefined,
    }

    return {
      onMapMounted: () => ref => {
        refs.map = ref
      },
      onZoomChanged: ({ onZoomChange }) => () => {
        onZoomChange(refs.map.getZoom())
      }
    }
  }),
  withScriptjs,
  withGoogleMap
)(props =>
  <GoogleMap
    defaultCenter={{ lat: -34.397, lng: 150.644 }}
    zoom={props.zoom}
    ref={props.onMapMounted}
    onZoomChanged={props.onZoomChanged}
  >
    <Marker
      position={{ lat: -34.397, lng: 150.644 }}
      onClick={props.onToggleOpen}
    >
      <InfoWindow onCloseClick={props.onToggleOpen}>
        <div>
          <FaAnchor />
          {" "}
          Controlled zoom: {props.zoom}
        </div>
      </InfoWindow>
    </Marker>
  </GoogleMap>
);

<MapWithControlledZoom />
```
