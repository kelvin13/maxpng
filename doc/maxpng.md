
###### Module

# MaxPNG

Efficiently decode, validate, and encode image data stored in the PNG format, and convert it to formats useful for common graphics libraries.

------

## Symbols

### Free functions


#### `func `[`png_decode`](functions.md#png_decode)`(path:String, recognizing recognized:Set<`[`PNGChunk`](pngchunk.md)`>)`

> Decompress, decode, and validate the raw pixel contents of a PNG file, without performing deinterlacing or deindexing.

#### `func `[`png_encode`](functions.md#png_encode)`(path:String, raw_data:[UInt8], properties:`[`PNGProperties`](pngproperties.md)`, chunk_size:Int) throws`

> Compress, encode, validate, and write the contents of a raw pixel buffer to a PNG file.

### Structures

#### `struct` [`RGBA`](rgba.md)

> A normalized color unit consisting of four color samples.

#### `struct` [`PNGProperties`](pngproperties.md)

> The non-pixel image data associated with a PNG file, as specified in the PNG standard.

#### `struct` [`PNGProperties.ColorFormat`](pngproperties_colorformat.md)

> The five PNG color formats, as defined in the [PNG standard](http://www.libpng.org/pub/png/spec/1.2/PNG-Chunks.html#C.IHDR).

### Classes

#### `class` [`PNGDecoder`](pngdecoder.md)

> A progressive PNG reader object that provides pixel data lazily, scanline by scanline, and closes all file and decompression streams when it goes out of scope

#### `class` [`PNGEncoder`](pngencoder.md)

> A progressive PNG writer object that encodes pixel data lazily, scanline by scanline, and closes all file and compression streams when it goes out of scope

### Enumerations

#### `enum` [`PNGChunk`](pngchunk.md)
> Public PNG chunks, as specified in the [PNG standard](http://www.libpng.org/pub/png/spec/1.2/PNG-Chunks.html).

#### `enum` [`PNGReadError`](pngerrors.md#PNGReadError:Error)
> Errors that may occur when reading and decoding a PNG file from disk.

#### `enum` [`PNGWriteError`](pngerrors.md#PNGWriteError:Error)
> Errors that may occur when writing and encoding a PNG file from disk.

#### `enum` [`PNGDecompressionError`](pngerrors.md#PNGDecompressionError:Error)
> Errors that may occur when decompressing a PNG `DEFLATE` stream.

#### `enum` [`PNGCompressionError`](pngerrors.md#PNGCompressionError:Error)
> Errors that may occur when compressing a PNG `DEFLATE` stream.