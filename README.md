# greasemonkey_video_speed
This is a Greasemonkey script that gives a small speed controller only on the sites you specifically choose.

Youtube started trying to charge for this as a way to upsell their subscription (lolwut, they can go eat dirt). This works for any primarily HTML5 based site, and also works for HTML5 audio (e.g. podcasts), though streaming music is normally not implemented as HTML5.

## Controls

Format is:

[keystroke] ("[button label]") = [function]

- S ("<<") = big step slower (-1x if current speed is >1x, else half the current speed, down to 0.125x minimum)
- s ("<") = small step slower (-0.1x down to 0.1x minimum)
- o ([the current speed]) = reset to 1.0x speed
- d (">") = small step faster (+0.1x up to 8x maximum)
- D (">>") = big step faster (+1x if current speed is >1x, else double the current speed, up to 8x maximum)

- v (no button) = toggle variable-speed ("breathe") mode. 

If switching between geometric ("S" and "D") to decimal ("s" and "d") increment sets, the speed snaps to the closest value of the new increment set that is still in the right speed direction (slower or faster).

Variable speed mode varies the playback between the current setting and 2x speed, allowing you to watch much faster average video speeds while giving your brain time to catch up and maintaining retention better even than watching on just 2x speed. I don't know fully why this works, but I've been doing it for years, and my suspicion is that it prevents your getting bored by a monotone consistent rhythm and then thinking of speech as background. 

Add or remove sites as desired from the front matter, or change the breathing intervals to be more to your liking.
