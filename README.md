<h1 class="display-4">Badge&#8203;Size&#8203;</h1>

This service creates badges based on the content length of any given file which is accessible, whether within your GitHub repository, npm package, CDN service or hosted your own endpoint.

Service Endpoint: [img.badgesize.io](https://badgesize.com)

The displayed size is based on the returned Content-Length returned by the files hosting siteof the file, by default this does not include the size of the returned headers but it will be the exact size that is your end-users will experience.

When requesting any compression type, if the hosting site doesn't support the requested compression then the size will (most likely) be the full uncompressed size (dependant on the file hosting service). There is also an internal maximum file-size for this case as most services do not return the Content-Length for compressed files.

To provide better scale while also reducing hosting costs, the files for a specific badge are fetched on-demand with any results internally cached to fulfil any subsequent requests. The caching mechanism uses a combination of cached number of elements in a FIFO style buffering where the minimum cache period is set to 24 hours, while also using any Cache-Control/Expires headers to provide longer periods when known. For example when using a CDN service that returns files from <code>npm</code> packages the internal Cache period and the resulting badge will be set to 1 year to reduce the number of requests made to the service.

## [Usage Details](https://badgesize.com/Usage)

See [Usage Details page](https://badgesize.com/Usage) to see how to format your URL and provide any optional parameters.

><hr />
> Usage is (mostly) compatible but slightly different from the previous implementation and has evolved some additional features.
><hr />

## [Examples](https://badgesize.com/Examples)

See [Examples page](https://badgesize.com/Examples) for a collection of simple example badges and how to include them within your repository readme files.

| Badge | Example
|-------|----------
| Default | ![Defaults](https://img.badgesize.com/nevware21/badgesize/main/README.md)
| Custom Label | ![Custom Label](https://img.badgesize.com/nevware21/badgesize/main/README.md?label=Custom%20label)
| GZip Size | ![GZip size](https://img.badgesize.com/nevware21/badgesize/main/README.md?compression=gzip)
| Brotli Size | ![Brotli size](https://img.badgesize.com/nevware21/badgesize/main/README.md?compression=brotli)<br/>**Note:** Github servers do not support brotli compression
| Any Compression | ![Any Compressed size](https://img.badgesize.com/nevware21/badgesize/main/README.md?compression=any)
| Any Compression with Custom Label |  ![Compressed size](https://img.badgesize.com/nevware21/badgesize/main/README.md?compression=any&label=Custom%20Label)
| Missing File | ![Missing File](https://img.badgesize.com/nevware21/badgesize/main/InvalidFilename?label=Missing%20File)

## Service Status 

> <hr />
>
> This is the location of the public portions of the new home for `img.badgesize.io`.
>
> Please use [this public GitHub repo](https://github.com/nevware21/badgesize) to create Issues or requests.
>
> <hr />
