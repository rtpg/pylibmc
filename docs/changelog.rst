Change Log
==========

New in version 1.5.0
--------------------

This release fixes critical memory leaks in common code paths introduced in
1.4.2. Also fixes a critical bug in a corner of the zlib inflation code, where
prior memory errors would trigger a double free. Thank you to everybody
involved in the making of this release, and especially `Eau de Web`__, without
their contributions, this release and the bug fixes it contains wouldn't have
been so expedient.

__ http://www.eaudeweb.ro/

New in version 1.4.0
--------------------

Brace yourself, Python 3.x support has come!

Thanks to everybody involved in this project; this release involves less
authors but **a lot** more work per person. Thanks especially to Harvey Falcic
for the work he put in, without which there wouldn't be any Python 3.x support.
Also thanks to Sergey Pashinin for the initial stab at the problem.

Other than that, we had miscellaneous bug fixes, testing improvements, and
documentation updates.

Last but not least I would like to ask for your support in this project, either
by helping out with development, testing, documentation or anything at all; or
simply by donating some `magic internet money`__ to the project's Bitcoin
address `12dveKhqiJWCY8zXT4kaHdHELXPeGAUo9h`__

__ http://static.adzerk.net/Advertisers/5af77cf0094d4303bb308b955dd05992.jpg
__ bitcoin:12dveKhqiJWCY8zXT4kaHdHELXPeGAUo9h

New in version 1.3.0
--------------------

Because there ain't nothing better than releasing software in the spring time.

Lots of improvements have come about in just about every corner of the library,
thanks to *eighteen different authors* over almost *20 pull requests*. Amazing.

- Added touch support
- Added compress_level
- Added weighted distribution
- Added automated benchmarking utility
- Added Travis CI and build status
- Added behavior dead_timeout
- Added behaviors tcp_keepalive
- Added behavior callback_prefix_key
- Lots of bug tuning, fixes, tests, and documentation

Lastly, thanks in particular to the authors of this release: Abramowitz,
Baklanov, Bergström, Borisov, Branson, Brown, Ericson, Hansche, Hlodversson,
King, Kowalak, McFague, Moura, Noguchi, Shurter, Williams and Wong.

New in version 1.2.0
--------------------

This release is for the people behind `reddit.com`__, for helping push
development forward. Keep doing your thing.

__ http://code.reddit.com/

- `semver.org`__ versioning scheme
- Fixed GIL issues
- Added CAS support (ketralnis)
- Added SASL authentication (Remoun)
- Added more detail to errors (spladug)
- Added mapping-like behavior for clients
- Fixed build errors on Mac OS X
- Moved to nose__ for testing
- Added ``auto_eject`` behavior
- Added ``num_replicas`` behavior
- Added ``remove_failed`` behavior
- Removed ``cache_lookups`` behavior
- Improved repr of clients (noah256)
- Improved IPv6 support (JshWright)
- Improved pooling behavior so it doesn't cause lock-ups
- Improved tests and testing foundation
- Improved documentation and structure
- Internalized Sphinx documentation
- Bunch of other stuff

__ http://semver.org/
__ http://somethingaboutorange.com/mrl/projects/nose/

New in version 1.1
------------------

- Removed deprecated space-based behavior names.
- Acquire and release the GIL properly, thanks ketralnis__
- Add support for ``libmemcached 0.40``
- Included a more useful command-line interface
- Fixed handling of NUL-byte keys in ``get_multi`` in binary protocol
- Fixed some valgrind-reported memory warnings
- Fixed bogus usage of time argument for delete.
- 1.1.1: Fixed tests under Python 2.5

__ http://www.ketralnis.com/

New in version 1.0
------------------

- Lots of documentation fixes and other nice things like that.
- Nailed what appears to be the last outstanding memory leak.
- Explicitly require libmemcached 0.32 or newer.

New in version 0.9
------------------

- Added a ``get_stats`` method, which behaves exactly like
  `python-memcached`'s equivalent.
- Gives the empty string for empty memcached values like `python-memcached`
  does.
- Added exceptions for most `libmemcached` return codes.
- Fixed an issue with ``Client.behaviors.update``.

New in version 0.8
------------------

- Pooling helpers are now available. See ``pooling.rst`` in the distribution.
- The binary protocol is now properly exposed, simply pass ``binary=True`` to
  the constructor and there you go.
- Call signatures now match `libmemcached` 0.32, but should work with older
  versions. Remember to run the tests!

New in version 0.7
------------------

- Restructured some of the code, which should yield better performance (if not
  for that, it reads better.)
- Fixed some memory leaks.
- Integrated changes from `amix.dk`, which should make pylibmc work under
  Snow Leopard.
- Add support for the boolean datatype.
- Improved test-runner -- now tests ``build/lib.*/_pylibmc.so`` if available,
  and reports some version information.
- Support for x86_64 should now work completely.
- Builds with Python 2.4, tests run fine, but not officially supported.
- Fixed critical bugs in behavior manipulation.

New in version 0.6
------------------

- Added compatibility with `libmemcached` 0.26, WRT error return codes.
- Added `flush_all` and `disconnect_all` methods.
- Now using the latest pickling protocol.

New in version 0.5
------------------

- Fixed lots of memory leaks, and added support for `libmemcached` 0.23.
- Also made the code tighter in terms of compiler pedantics.

New in version 0.4
------------------

- Renamed the C module to `_pylibmc`, and added lots of `libmemcached` constants
  to it, as well as implemented behaviors.
