+++
title = 'JBD Bms'
date = 2025-06-04T11:42:13-07:00
draft = false
+++

There are a few sections which are unfinished. In the future I might fill them in or if you know the correct description for what is left out then submit a pull request on [github](https://github.com/nate0m/www/blob/main/content/post/JBD-bms.md).

## Brief Introduction

JBD bms’s are popular inexpensive battery management systems that are sold on [jiabaida’s website directly](https://jiabaida-bms.com/) but are more commonly purchased on aliexpress. This is my first experience with a JBD bms and this is also my first fully custom battery build. I found that due to language barriers the JBD app which is used to set the parameters for your battery is slightly unintuitive and confusing. That is why this document exists. 

My battery build is 20s so I went with the Jiabaida SP22S003B which can accommodate up to 22s and have different wiring diagrams for each step. [Wiring Diagrams Here.](https://jiabaida-bms.com/blogs/content/jiabaida-sp22s003b-smart-bms-wiring-diagram?spm=a2g0o.detail.1000023.4.6d1330b03TSyat) 

## Wiring

Follow the wiring diagrams for the balance cables. If you are not populating all 22 possible balance wires, it boils down to 21 & 22 stay individual while you can string 20-4 together depending on how many cells you are putting in series.

![wiring diagram](/img/post/JBD-bms/1.png)

### Main Positive and Negative
- B- goes to the main neg of your battery  
- Your neg charging and discharge cables go to C-  
- Your pos charging and discharging cables go to the main pos of the battery

## The App

### Different Chemistries

![app page 1](/img/post/JBD-bms/2.png)

If you buy this bms wanting to use it for li-ion and you have trouble with the cells only charging to 3.6v then what you need to do is go to the `Protection Param` settings page and at the top right there is a `switch to LFP` or switch `to NPM` ‘button’. You want to be on LFP so you want to see the NPM ‘button’. But even if you already see it and your cells are still not charging above 3.6 then just press the ‘button’ and press it again to go back to LFP. That fixed it for me.

### Origin Settings

![app page 2](/img/post/JBD-bms/3.png)

Nominal capacity: The capacity of your battery  
*Cycle capacity: I think auto fills*  
*Full charge capacity: I think auto fills*  
Cell num: will auto fill

### Protection Param

![app page 3](/img/post/JBD-bms/4.png)

CellHighVoltProtect: a little above max voltage of a single cell  
CellHighVoltRecover: a little below max voltage of a single cell  
CellHighVoltDelay: default  
CellLowVoltProtect: the lowest you want a cells voltage to go  
CellLowVoltRecover: a little above CellLowVoltProtect value  
CellLowVoltDelay: default  
TotalVoltHighProtect: a little above the maximum voltage of your battery  
TotalVoltHighRecover: a little below the maximum voltage of your battery  
TotalVoltHighDelay: default  
TotalVoltLowProtect: a little below the minimum voltage of your battery  
TotalVoltLowRecover: a little above the minimum voltage of your battery  
TotalVoltLowDelay: default  
HwCellHighVoltProtect: idk (looks like the actual max voltage of a cell)  
HwCellLowVoltProtect: idk (looks like the actual low voltage of a cell)

### Capacity Voltage

![app page 4](/img/post/JBD-bms/5.png)

This is based on your specific cells (check the datasheet).

## Misc.

I also had an issue where I could not activate the discharge port. I ended up going into the function settings and disabled switch settings which automatically activated discharge and charge functionality. 
