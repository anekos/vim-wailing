Vim Wailing
===========

I honestly don't have a better name for this. It's inspired by the likes of <http://www.finaldeadline.co.uk/scrawl.html> and Write To Die. It has these external dependencies:

* **mpv** - For alarm playback and control.
* **socat** - For alarm playback and control.
* **bash** - For the optional timed feature. I'm positive there's a better way to do this using a more barebones shell.

To use this, this exposes three user commands:
* **SetupWailing** - Have the plugin monitor your typing when you're in insert
mode (specifically) for the current buffer so it can yell at you when you aren't.
* **SetupWailingTimed** - Same as the previous, except it also accepts hh:mm:ss, mm:ss, and seconds.
* **TeardownWailing** - Stop the plugin from yelling at you when you stop typing.

The plugin cleans itself up when you quit the buffer you set it up on.
Lastly, there is one option you'll need to set in your .vimrc:
* **g:wailing_alert_fpath** - The filename for what the program should be yelling at you with.

There are three additional options that you may also want to set:
* **g:wailing_reward_fpath** - The filename for what the program should reward
you with after you finish your session. Rewarding you with a session complete
sound will NOT occur if you don't set this (vs having the plugin annoy you).
* **g:wailing_reward_start** - The time the reward should start at in the specified
reward file. (in seconds)
* **g:wailing_reward_end** - How long the reward should be playing (in seconds)
