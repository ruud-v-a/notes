CUE Splitting
=============

The new way:

    ~/dotfiles/split-cue.py album.cue

See also <https://github.com/ruuda/dotfiles/blob/master/split-cue.py>. This
script relies on binaries from the `cuetools` package on Arch.

The old way: to split album.flac to the tracks in album.cue as wav files, then
encode at the highest compression setting:

    $ shnsplit -f album.cue -t '%n - %t' album.flac
    $ flac -8 *.wav

The program `shnsplit` is part of the `shntool` package on Arch. The `-t` flag
sets the output filename: `%n` is the track number, `%t` the title.
