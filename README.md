# ssl_redirect option in Progressive accessibility alias

<p align="center">
  <img width="256" height="256" src="https://github.com/skrypte/elm-hn-pwa/raw/master/dist/ico/hn_256.png">
</p>

HNPWA implementation leveraging [Elm](http://elm-lang.org) 0.18 compiler with upstream [Hacker-News API](https://github.com/HackerNews/API) integration.

Live instance: [hnpwa.skingrapher.com](https://hnpwa.skingrapher.com)

## Performance Metrics

- [lighthouse](https://hnpwa.skingrapher.com/lighthouse.html) score: **100/100**
- [webpagetest](https://www.webpagetest.org/result/171012_1D_2e14b74f9e034fb5d5f2e88891be0791/) 3G throttled: **91/100**
- [workbox](https://workboxjs.org)-generated service worker handles static asset precaching
- HN data persisted offline via IndexedDB
- SSR not implemented (client-side hydration only)

**Interactive Benchmarks**:
- Emerging markets (Moto 4G/3G): 4.8s
- Standard 3G: 3.2s

## Design System

Stylesheet architecture:
- [Sass](https://sass-guidelin.es/) preprocessor
- [Material Design Lite](https://getmdl.io/components/index.html) component patterns
- < 4kb minified + inlined in `index.html`
- Responsive grid supports mobile/tablet/desktop viewports

## Accessibility Compliance

- Lighthouse accessibility audit: **100/100**
- WCAG 2.0 Level AAA conformance
- Contrast ratios exceed AAA thresholds
- [WAI-ARIA 1.1](https://www.w3.org/TR/wai-aria-1.1/#feed) **feed** role with **aria-posinset**/**aria-setsize** attributes
- [a11y.css](https://ffoodd.github.io/a11y.css/) validation passes
- Vector-only assets (no raster images)
- External links utilize **noopener**/**noreferrer** to mitigate tabnabbing attacks

## Release Notes

**v0.11**: Stable build excluding pagination feature

## Roadmap

- Background Sync API testing
- Virtual scrolling for deeply nested comment threads

## Compilation

Generate `elm.js` artifact:

    elm make Hnpwa.elm --output elm.js

Minified output gets embedded into `index.html` `<script>` block.

## References

- PWA fundamentals: [Google Developers](https://developers.google.com/web/progressive-web-apps/)
- Curated resources: [awesome PWA](https://github.com/hemanth/awesome-pwa)
- Elm SPA patterns: [client elm](https://github.com/foxdonut/adventures-reactive-web-dev/tree/elm-010-todolist-feature/client-elm) (Fred Daoud), [elm spa example](https://github.com/rtfeldman/elm-spa-example) (Richard Feldman), [elmstagram](https://github.com/bkbooth/Elmstagram) (Ben Booth)
- Service Workers: [MDN documentation](https://developer.mozilla.org/en-US/docs/Web/API/Service_Worker_API)

## Attribution

- GitHub icon: [Entypo](https://entypo.com) iconset
- Elm logo: [Wikimedia Commons](https://upload.wikimedia.org/wikipedia/commons/f/f3/Elm_logo.svg)
- Loading spinner: [Sam Herbert](http://samherbert.net/svg-loaders/) SVG collection
