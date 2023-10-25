### Obsidian Plugins
**Better PDF**
```pdf
{
	"url" : "/path/to/file.pdf"
	"link" : false //true or false
	"page" : 1 //1 or [1, [3, 6], 8] where [3, 6] is an inclusive range of pages. page = 0 is an alias for the whole document
	"range" : [1,3] // [1, 3] Insert pages 1 to 3 (inclusive). Overwrites page.
	"scale" : 1.0 //0.5 for 50% size or 2.0 for 200% size
	"fit" : true //true or false
	"rotation" : 0 //90 for 90deg or -90 -90deg or 180
	"rect" : [0,0,0,0] //offsetX, offsetY, sizeY, sizeX in Pixel
}
```

