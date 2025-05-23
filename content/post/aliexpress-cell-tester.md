+++
title = 'Aliexpress Cell Tester'
date = 2025-05-22T16:13:28-07:00
draft = false
+++

![aliexpress page](/img/post/aliexpress-cell-tester/2.png)

### The Need for a Cell Tester
Recently I started harvesting cells from discarded ebike batteries. Naturally this meant that I needed a way to test the health of these cells. When you test the health of a cell there are a few things that you need to check that being the capacity, maximum voltage, and internal resistance. Most important being the capacity as this is the amount of charge the cell can hold and directly relates to the amount of energy the cell can hold. 

### The Function of a Cell Tester
The main way to test capacity of cells is to use a cell capacity tester. This is a device that will charge the cell to maximum voltage using a constant current then run the cell down to a minimum voltage with a constant current during the draining process it keeps track of the amount of watts the cell is outputting and the amount of time that passes and give you the amount of energy that the cell output in watt hours which is a unit of energy. It also measures the amount of amps which is being output and gives you the amount of charge the cell output in milliamp hours which is a unit of charge. When I say constant current all that means is that we are discharging the same amount of amps from the cells as the voltage of the cells changes. 

### Amazon Options
There are a lot of options on amazon for these kinds of cell capacity testers. But most of them have the same drawbacks and are difficult to discern the exact features from the product page. You might have a four or eight slot charger that is capable of capacity testing, but only with a select number of slots. The only one that I could find on amazon that had the ability to capacity test on all eight cells was [this one](https://a.co/d/1zsVtpr). But it has one major drawback. If you load up all eight of the slots you can only charge and discharge at 0.5amps, which is very slow for testing tens to hundreds of cells, and it’s $80 which seems reasonable but once you compare it to what I ultimately ended up buying it seems pricey. It will take you all day to test only eight cells. I actually never ended up buying this cell tester. I bought a [different one](https://www.amazon.com/dp/B09KN4RJ3F?ref=ppx_yo2ov_dt_b_fed_asin_title) that I thought had the same number of features but it ended up only being able to load test on four of the eight cell slots. Then I bought [two small four cell testers](https://a.co/d/cqRs9DX) that I also thought could load test in all four slots, but again I was fouled and they could only load test in one slot each to my dismay.

### I Found... The One
This eventually led me to aliexpress. Which was also sparse for options. I had previously bought a four cell tester on ali and was using it before I bought the ones on amazon but it ended up dying. I think I plugged it into a pd usb-c power supply when it only accepted 5v 2amps, whoops. Eventually I found a tester on ali that met all of my needs. It was eight slot, it could accommodate 21700 cells, and could load test each cell at 1amp (which would be fast enough).

### Less of a Product But still good
The one that I bought was a little bit more than this one and you have to buy a 5v 10amp barrel jack power supply for it as well, so all together it cost me like 60$. A fair bit cheaper than the amazon option, but this is a lot less like a finished product and more like an engineering sample vs something made for a mass market. The back cover has no sides, the top has exposed contacts and ribbon cables, not to mention how I had to make my own solution to mounting the 21700 cell holders. Also make sure that you buy a high quality power supply because I bought a cheap one and when I load test 8 cells that are all at a low voltage the unit shuts off. I have to replace some of the lower voltage cells with high voltage ones or completely take out a cell on each side. 

![aliexpress page](/img/post/aliexpress-cell-tester/1.png)

### Modifications
It’s a great cell tester with many features but it needed some modification before it was ready to be put into my workflow. 

It also does not come with an easy way to mount the 21700 cell trays on the unit. I ended up designing and 3D printing sleeves that slide over the 18650 trays and vhb’ed the 21700 trays to the top of the sleeve. Along with some xt30 connectors, solid core wire. I also 3d printed some triangle pieces to prop the whole unit up at a ~45 degree and vhb’ed those to the back. You can see the end product at the beginning of this post.

The best thing about this cell tester is that when you capacity test a cell it will not fully charge it at the end of the cycle. Once the capacity of the cell is tested it will drain the cell to a set voltage for storage. 

### Somes notes on how to actually use the cell tester

There is no on/off switch, when you plug it in it just turns on.

You have the M button which switches between the 8cell view and the single cell view. 

![cell tester after mods](/img/post/aliexpress-cell-tester/3.png)

If you long press the M button it opens up the menu for chn1 from here you can set chn1 to sync with all the other channels so that you only have to set the parameters once. 

![cell tester after mods](/img/post/aliexpress-cell-tester/4.png)

From here you set the mode AUTO for capacity testing, DSG for discharging, CHG for charging, and ACTI for activation which is some type of forced charging that I do not use. From here you can also set the max charge voltage which is VOLT1 and the finishing or storage voltage which is VOLT2 as well as the stop voltage which is the lowest you want to discharge, idle time which is just an amount of time that the cell rests between charge and discharge cycles. 

To test cells simply load in the cells that you want to test use the CHN button to select the slot you have filled and press the R/S to start or stop the test or if you load all eight slots press and hold the R/S button and it will start all eight slots simultaneously. You will see the voltage amps being draw or put into and capacity of each cell on the display as well and how long the test has been running.

### Closing remarks
In my opinion this is a much better deal for a more advanced piece of equipment compared to anything I was able to find on amazon. 

If you are looking to recreate this setup including the 3D printed pieces that I designed here is a link to a printables page with the files. If you want to purchase the cell tester on aliexpress just search `18650 load tester` and pick the one that comes with the 21700 trays. I won't put a link here because aliexpress links almost always end up dying.




