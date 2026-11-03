# ding

An alarm that turns a deadline into a timer. Tell it *when* something is due, and it counts down
the time left, dinging at 50%, 75%, 90%, 95% and 100% of the way there.

```
                                ⏰ Tue 23:59:00

                                     10:00
                               remaining of 20:00

           █████████████████████████░░░░░░░░░░░░┃░░░░░░┃░░┃░░   50.0%

                     ● 50%   ○ 75%   ○ 90%   ○ 95%   ○ 100%

                               next ding 23:54:00

       \    /\
        )  ( ')
       (  /  )
 —sea   \(__)|
```

## Usage

```sh
ding today at 23:59      # → e.g. a 20-minute timer, if it's 23:39 now
ding 23:59               # a time already past today rolls over to tomorrow
ding tomorrow at 7:30
ding at 9pm
ding 20m                 # plain durations work too: 90s, 20m, 1h30m
```

It runs full-screen. Each milestone plays a sound and shows a notification; at 100% it waits for
Enter. `Ctrl-C` cancels.

## Install

Needs Python 3 and nothing else.

```sh
git clone https://github.com/kotongit/ding.git
ln -s "$PWD/ding/ding" ~/.local/bin/ding    # any folder on your PATH works
```

Currently macOS only: sounds use `afplay` and notifications use `osascript`.

## Credits

The cat is by **Joan G. Stark** (signed `jgs` in the original), from her ASCII art collection.
Here it's re-signed `—sea`, with thanks and credit to her.

## License

[MIT](LICENSE)
