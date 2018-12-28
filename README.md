# @syncromatics/react-google-maps

A fork of [react-google-maps][upstream] for displaying and interacting with Google Maps in React applications

## Quickstart

Add the `@syncromatics/react-google-maps` package to your project:

> With `yarn`:
> 
> ```sh
> yarn add @syncromatics/react-google-maps
> ```

> With `npm`:
> 
> ```sh
> npm install --save @syncromatics/react-google-maps
> ```

Then use it to display maps:

```js static
import { GoogleMap, Marker } from "@syncromatics/react-google-maps"

const MyMapComponent = (props) =>
  <GoogleMap
    defaultZoom={8}
    defaultCenter={{ lat: -34.397, lng: 150.644 }}
  >
    {props.isMarkerShown && <Marker position={{ lat: -34.397, lng: 150.644 }} />}
  </GoogleMap>

// Uses of MyMapComponent
<MyMapComponent isMarkerShown />// Map with a Marker
<MyMapComponent isMarkerShown={false} />// Just only Map
```

Continue [reading the documentation][documentation] for more interactive examples of interactions with Google Maps.

### Getting Help

The [documentation][documentation] has examples of how to use each component. Many people have asked and answered questions on [StackOverflow](https://stackoverflow.com/search?q=react-google-maps). (Some things may be general Google Maps issues, for which there are [lots of questions and answers](https://stackoverflow.com/questions/tagged/google-maps?sort=votes&pageSize=50) as well.)

## Building

[![Travis](https://img.shields.io/travis/syncromatics/react-google-maps.svg)](https://travis-ci.org/syncromatics/react-google-maps)
[![npm](https://img.shields.io/npm/v/@syncromatics/react-google-maps.svg)](https://www.npmjs.com/package/@syncromatics/react-google-maps)
[![devDependency Status](https://img.shields.io/david/dev/syncromatics/react-google-maps.svg)](https://david-dm.org/syncromatics/react-google-maps#info=devDependencies)

Install dependencies:

```bash
yarn
```

Run React Styleguidist, a hot-reloading interactive local website:

```
yarn styleguide
```

Once the styleguide is running, visit http://localhost:6060 and start coding! (Note, you should probably get an API key with the Google Maps API enabled, then update [`constants.js`](src/docs/constants.js).)

Learn more in our [contributor's guide](CONTRIBUTING.md).

## Code of Conduct

We are committed to fostering an open and welcoming environment. Please read our [code of conduct](CODE_OF_CONDUCT.md) before participating in or contributing to this project.

## Contributing

We welcome contributions and collaboration on this project. Please read our [contributor's guide](CONTRIBUTING.md) to understand how best to work with us.

## License and Authors

[![GMV Syncromatics Engineering logo](https://secure.gravatar.com/avatar/645145afc5c0bc24ba24c3d86228ad39?size=16) GMV Syncromatics Engineering](https://github.com/syncromatics)

[![license](https://img.shields.io/github/license/syncromatics/react-google-maps.svg)](https://github.com/syncromatics/react-google-maps/blob/master/LICENSE)
[![GitHub contributors](https://img.shields.io/github/contributors/syncromatics/react-google-maps.svg)](https://github.com/syncromatics/react-google-maps/graphs/contributors)

This software is made available by [Tom Chen][upstream] under the MIT license and this fork is maintained by GMV Syncromatics Engineering.

[upstream]: https://github.com/tomchentw/react-google-maps
[documentation]: https://syncromatics.engineering/react-google-maps/#introduction