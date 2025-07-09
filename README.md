# Want to see it live?
**See the live version of the code here: <https://zlatkovsky.github.io/DOMPurifyMystery>**

<hr />

# The mystery: `foreignObject` contents getting stripped

This repo demonstrates a now-figured-out mystery with DOMPurify: of how the `foreignObject` contents were getting stripped by more recent `3.x` versions of DOMPurify (e.g., `3.2.6`), even though they worked in earlier `3.x` versions (e.g., `3.1.4`).
> See related issue and the corresponding `HTML_INTEGRATION_POINTS` workaround: [DOMPurify 3.1.7 breaks Mermaid diagrams using foreignObject](https://github.com/cure53/DOMPurify/issues/1002).

Note that in DOMPurify `2.x` (e.g., `2.5.7`), the contents ends up getting stripped out regardless of any config settings.

<br />

# A side issue of "sticky" config settings

The repo also demonstrates an issue with some DOMPurify settings being "sticky" (e.g., once HTML integration points are enabled once via config, they continue to be set even for future invocations of `DOMPurify.sanitize`).
> See the issue I just filed on July 9 2025: [Some settings (e.g., HTML_INTEGRATION_POINTS, and likely others) are "sticky"](https://github.com/cure53/DOMPurify/issues/1119).
