# greasemonkey_video_speed
This is a Greasemonkey script that gives a small speed controller only on the sites you specifically choose.

Youtube started trying to charge for this as a way to upsell their subscription (lolwut, they can go eat dirt). This works for any primarily HTML5 based site.

## Controls

Format is:
[keystroke] ("[button label]") = [function]

S ("<<") = big step slower (-1x if current speed is >1x, else half the current speed, down to 0.125x minimum)
s ("<") = small step slower (-0.1x down to 0.1x minimum)
o ([the current speed]) = reset to 1.0x speed
d (">") = small step faster (+0.1x up to 6x maximum)
D (">>") = big step faster (+1x if current speed is >1x, else double the current speed, up to 6x maximum)

If switching between geometric ("S" and "D") to decimal ("s" and "d") increment sets, the speed snaps to the closest value of the new increment set that is still in the right speed direction (slower or faster).

Add or remove sites as desired from the front matter.
