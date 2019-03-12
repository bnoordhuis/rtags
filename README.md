# rtags

My `ctags` wrapper for Rust code. Shamelessly cribbed from other ctags wrappers.
I claim no copyright. :-)

## Usage

Put the `rtags` shell script on your path and execute the following commands
from the root of your project:

    $ rtags -R .

    $ cargo update

    $ rtags -f $HOME/rust.tags -R $HOME/.cargo/registry/src/*/*/src

Then add this stanza to your `.vimrc`:

    set tags=tags,$HOME/rust.tags

Now `^]` and `g]` will list definitions from your own project and your
dependencies.

## Notes

`rtags -e` should emit Emacs-compatible tag files although I've never tried. :-)
