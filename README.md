# smi2vtt
Convert `.smi` to `.vtt`  
(This module doesn't supported stylesheet)


## Installation

    $ npm install smi2vtt

## Usage

server.js
``` js
const smi2vtt = require('smi2vtt')
const app = express()

app.get( '/smi/:filename', (req, res) => {
  // parse
  smi2vtt( req.params.filename )
  // send
  .then( data => {
    res.set( 'Content-Type', 'text/vtt' )
    res.send( data )
  })
})
```

index.html
``` html
<video width="100%" controls>
  <source src="video/01.mp4" type="video/mp4">
  <track src="smi/01.smi" kind="subtitles" srclang="ko" label="korean" default>
</video>
```
