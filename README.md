# Analytics

Analytics is a plugin for [Kite](https://github.com/kite-plus/kite) that
counts a site's visits with one of four services:

- [Baidu Tongji](https://tongji.baidu.com)
- [Google Analytics](https://analytics.google.com)
- [Umami](https://umami.is), its cloud or your own
- [Plausible](https://plausible.io), its cloud or your own

A preview on your own computer, at `localhost`, is not counted unless you
say so in the settings.

## Using it

Drop the zip of a release on the upload tile under **Plugins** in Kite's
studio, or add it from the command line inside a site:

```sh
kite plugin add analytics-0.1.0.zip
kite plugin enable analytics
```

Then choose the service under **Plugins → Analytics → Settings** and fill in
what it asks for: the site code Baidu gives you, the measurement ID of a
Google Analytics web stream, an Umami website ID, or the domain a site is
added under in Plausible.

The plugin asks for Kite 1.0 or later.

## Releasing

`make zip` packs `dist/analytics-<version>.zip`, which the studio installs as
it is. Check it with `kite plugin verify .`, then tag the release and attach
the zip.

## License

[Apache License 2.0](LICENSE).
