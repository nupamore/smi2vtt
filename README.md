# smi2vtt
Convert `.smi` to `.vtt`  
(This module doesn't supported stylesheet)


##Installation

    $ npm install smi2vtt

##Usage
``` js
const smi2vtt = require('smi2vtt')
const app = express()

app.get( '/:filename', (req, res) => {
  // parse
  smi2vtt( req.params.filename )
  // send
  .then( data => {
    res.set( 'Content-Type', 'text/vtt' )
    res.send( data )
  })
})
```
