useMediaStore hook
==================

Use this hook to connect your componeny with the media store.

```es6
import useMediaStore from '../../components/hooks/use-media-store';

function MyComponent() {
	const mediaSourceId = '<the-media-store-id-here>';
	const { isPaused, play } = useMediaStore( mediaSourceId );

	return (
		<div>
			{ `The media is ${ isPaused ? 'paused' : 'playing' }.` }
			<Button onClick={ play }>Play media!</Button>
		</div>
	);
}
```

the `useMediaStore()` expect a valid media source ID as parameter, and it returns an object with properties and helper functions:

### isPaused

-   Type: `boolean`

True is the media is currently paused. Otherwise, False.

### currentTime

-   Type: `integer`

Current playing time of the media, in milliseconds.

### play()

-   Type: `function`

Use this helper function to play the media.

### pause()

-   Type: `function`

Use this helper function to pause the media.

### toggle()

-   Type: `function`

Use this helper function to play the media when it's paused, and vice versa.