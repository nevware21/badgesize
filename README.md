<h1 class="display-4">Badge&#8203;Size&#8203;</h1>

This service creates badges based on the content length of files which lives in your repository, npm package or CDN.

The reported size is based on the returned Content-Length by the site / CDN used to fetch requested file, by default this does not include the size of the returned headers but it will be the exact size that is your end-users will experience.

## Known differences from previous version

- The reported size for the GZip and Brotli compression is based on the size reported by the site / CDN used to fetch the requested file, this provides a more accurate representaiton of the download impact / experience that your end-user / consumers will experience from the previous version (which used local compression).
- Does not support PNG response
- Does not support JSON response
- It uses a longer Cache-Control period to assist with reducing the overall costs of maintaining this service.
- Badges are automatically added to images based on the source of the file.
- Provides a generic compression type `any` which can be used to return your site / CDN's default compression algirithm.

## Service Status 

> <hr />
>
> <b>The site and service is incomplete and under construction.</b>
>
> This is the location of the public portions of the new home for `img.badgesize.io`.
>
> An alpha version of the site and services is currently undergoing testing and evaluation to ensure that we can provide a better experience for our users without excessive overheads, the new version does not use the same code as [previously published](https://github.com/ngryman/badge-size) instance, but it does provide a compatible syntax with a simular set of features.
>
> There is no defined timeframe for when this service will move out of it's alpha state and restart with a higher level of support, as it is still under construction / evaluation.
>
> Please use [this public GitHub repo](https://github.com/nevware21/badgesize) to create Issues or requests.
>
> <hr />
