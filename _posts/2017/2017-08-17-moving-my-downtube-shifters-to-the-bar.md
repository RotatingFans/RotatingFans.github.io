---

layout: "post"
title: "Moving my Downtube shifters to the Bar"
date: "2017-08-17 21:37"
Categories: [3D]
---
![The final Product](/static/assets/img/blog/2017/08/DSC_6788_WebRes.JPG)

My family had an old Fuji Ace from the 80s that hadn't seen much use in years. I decided to see if I could ride it. After new tires and tubes, it rode, but I simply could not feel comfortable reaching down so far to shift. I figured it couldn't be too hard to move the shifters. After some research and a trip to my local bike shop, I had the parts I needed to let them reach the bar, but I still needed a way to mount them to the bar. I then began a multi-day design and prototyping journey.

I searched thingiverse and found a good [bracket](https://www.thingiverse.com/thing:224743) to base my design around. It even had a hinge to make installation easier. I opened up FreeCAD and designed the shifter block. I then put it and the bracket into a single model using blender. I did a quick print on the 3D printer to test the fit and two issues. The hole was too wide to thread the screw into and the bracket itself was too wide to create a snug fit on the bike. No worries, the bracket was designed in OpenSCAD which made it quite easy to decrease the size slightly.

![The shifter block brackets](/static/assets/img/blog/2017/08/DSC_6815_WebRes.JPG)

After getting the shifter block working and mounted, I realized I needed a cable stop for the housing. I figured I could repeat the design of the shifter block, but change it to be a cable stop instead. After a print, I was drilling holes because I had made them far too small in the design.

![The cable stop](/static/assets/img/blog/2017/08/DSC_6820_WebRes.JPG)

Once sizing was correct, I began functional testing. After multiple failures at the hinge, I increased the size of the hinge to allow for better infill between the two sections.

![Example of a break in the hinge](/static/assets/img/blog/2017/08/DSC_6825_WebRes.JPG)

With the larger hinge, the front shifter(My test dummy) shifted. I turned the bike over and rode up and down the street until the peg on the shifter block sheared right off.

![The two pieces sheared off](/static/assets/img/blog/2017/08/DSC_6827_WebRes.JPG)

I choked it up to a failure in the print and increased perimeter-infill overlap and reprinted the bracket. It then did not fail. YAY!

Now it was time to start the rear shifter. I held off on this because it is indexed, so precision of the shifter is much more important and the front shifter should require more force. Test strength then precision was my thinking. I replicated my front shifter setup and realized the cable block needed to be turned around so the hinge was on the correct side of the bar. I printed this new bracket and made the mistake of only mirroring the cable stop, not the hinge bracket. This resulted in a bracket that could not go together.

![The hinge was on the same side of both brackets](/static/assets/img/blog/2017/08/DSC_6823_WebRes.JPG)

After fixing that issue, installation went well, but shifting was quite clunky - less than ideal. Due to the pull on the cable stop, the cable stop would move towards the shifter without actually moving the cable.

At this point, I decided to change from the clunky FreeCAD and Blender solution to OpenSCAD. After scripting the parts, I extended the bracket's height and changing from the hinge to bolt hole on both sides for the extra strength. Installing this bracket greatly helped the rear shifter towards smooth shifting.

![The new all in one bracket](/static/assets/img/blog/2017/08/DSC_6797_WebRes.JPG)

At this point I took it on a longer ride around the neighborhood. The peg on the front shifter block sheared off halfway through the ride.

To combat the stress  being put on the peg, I increased the depth the base block and changed out the built-in thumbscrews on the shifters with normal screws. This was a ~~painful~~ fun process of getting them to the correct length. After 6 screws and two trips to home depot, the screws were the correct length. During my trials of screw length, I managed to strip the holes in the shifter blocks due to their limited depth. I went to print another copy of each and ran of filament halfway through. The next day I printed them in orange which actually ended up looking okay as a final product.

While I had the rear shifter unscrewed, I could see how it functioned. It is very simple, a small ball bearing travels over little groves. By putting it in indexed mode, this bearing is pushed into the groves as opposed to friction where it doesn't touch them.

![The inside peices of the shifter](/static/assets/img/blog/2017/08/DSC_6776_WebRes.JPG) ![The inside plate of the shifter](/static/assets/img/blog/2017/08/DSC_6779_WebRes.JPG)

When installing these new brackets I needed to remove the cables, but at this point I had already cut and crimped them. After some thinking, I cut a small slot into the cable stop to pull the cable out sideways through to make for easier replacements.

The files are available for download on [thingiverse](https://www.thingiverse.com/thing:2489916).

I printed the pieces in Hatchbox PLA at 75% infill, .2mm layer height with 3 perimeters, supports, and a rectilinear infill pattern
