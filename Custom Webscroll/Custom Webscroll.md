The Webkit-based browsers like Safari and Chrome .

- The selectors are

```css
body::-webkit-scrollbar {
		width: 1em; 
}
		
body::-webkit-scrollbar-track { 
		box-shadow: inset 0 0 6px rgba(0, 0, 0, 0.3); 
} 

body::-webkit-scrollbar-thumb { 
		background-color: darkgrey;
		 outline: 1px solid slategrey;
}

```

The `-webkit-scrollbar` family of properties consists of _seven_ different pseudo-elements that, together, comprise a full scrollbar UI element:

`::-webkit-scrollbar` for background
`::-webkit-scrollbar-button` For the directional buttons
`::-webkit-scrollbar-track` empty space below the progress bar
`::-webkit-scrollbar-track-piece`  top-most layer of the the progress bar
`::-webkit-scrollbar-thumb` the Draggable button element
`::-webkit-scrollbar-corner` bottom corner of the scrollable element
`::-webkit-resizer`  addresses the draggable resizing handle that appears above the `scrollbar-corner` at the bottom corner
