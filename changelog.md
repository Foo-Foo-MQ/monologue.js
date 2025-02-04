## v2.0.0
* Add support for node 16+
* Remove support for node 10

## v1.0.1
* Add support for node 15

## v1.0.0
* Add support for node 14
* Dropped support for node 8
* Update documentation to match ownership of Foo-Foo-MQ

## v0.4.0
* Convert to node only version of the lib... This is the first published version of this forked version of [monologue.js](https://github.com/postaljs/monologue.js)

## v0.3.5
* Remove unnecessary _.bind call that seems to contribute to memory/garbage

## v0.3.3
* Fixed issue where cache array held undefined values (due to subscriber removal).
* Updated gulpfile to format prior to combining

## v0.3.2
* Fixed issue where downstream once() subscribers were breaking the iteration of a publish over a list of subscribers.
* Added JSCS formatting, updated gulp tasks.

## v0.3.1
* Fixed bug where listeners were incorrectly added to another topic's lookup cache when adding a new subscriber for an event that had already been published once.

## v0.3.0
* Ported postal's caching mechanisms (mostly) to monologue to optimize for emitting
* Ported postal's subscription definition prototype (mostly) to better align subscription configuration options
* Added tests & test coverage monitoring

## v0.2.1
* the `Monologue.mixInto` method now utilizes [riveter's](https://github.com/a2labs/riveter) `punch` call under the hood. This is a change from v0.2.0 when it used riveter's `mixin` call, which would NOT overwrite target methods with the same name as methods from Monologue's prototype. Now the `mixInto` call *will* overwite target methods with Monologue's.

## v0.2.0

* Updated the bindings resolver to match that of [postal.js](https://github.com/postaljs/postal.js) v0.10
* Now utilizing [riveter](https://github.com/a2labs/riveter) for inheritance/mixin concerns
* Replaced underscore dependency with lodash
* Converted build to gulp.js
* Removed the "lite" build option
