# Teaser image
![fixedit](https://user-images.githubusercontent.com/1096409/136587337-c3030eec-17dc-487b-97b4-d6835abfb37c.jpg)

### Why?
The yoke is .. fine .. but I do not like the haptic controls at all. I've driven @ 5k miles, and they just aren't good. I decided to fix it for myself, and will share my work.

The Plaid uses a lot of the parts bin from the Model 3/Y, and that's a great thing! The electrical architecture of the Plaid is basically just that of an oversized Model 3, which is a smart move for manufacturing simplification.

### Notes
* The left stalk (signals/brights/wipers) is fully functional. The other side is a work in progress, but I've validated I can change gear via software, so I just need to wire everything up.
* You cannot just put a Model 3 or Y clockspring/SCCM into a Plaid and make it work. The refresh S ignores the CAN messages from this, and more importantly the car refuses to go into drive with an SCCM running firmware it doesn't like.
* The stalk modules can be removed and fit perfectly into the Plaid SCCM because it is literally the same part number as the 3/Y SCCM. You cannot just plug the ribbon cables in, however, since the Plaid's firmware doesn't try to report on the stalks, so they'll just look pretty without doing anything.
* I wrote custom firmware that uses a Particle Photon + Carloop device to send messages that the plaid expects. This took a bit of reverse engineering and I'll post the info to the github link as time allows. I will not directly help anyone who wants to do this, but I wish you luck. It should be relatively easy once I work out the remaining kinks.
* This change is entirely reversible, and no stock hardware is permanently modified. The shrouds with cutouts for stalks are directly out of a Model 3, and the Plaid shrouds are untouched.

# Video
[![YouTube: Exmaple of it doing things](https://img.youtube.com/vi/6T2n5DXqf1k/0.jpg)](https://www.youtube.com/watch?v=6T2n5DXqf1k)
