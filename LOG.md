# Debug log

Your notes. One entry per bug you fixed, using the template below.

This file is read as carefully as your code. A correct fix you cannot
explain counts for little; a bug you could not fix but investigated
honestly still counts for something.






## CC-02 — "Can't read anything in dark mode"

**Reproduced:** opened the site in dark mode , the price and name of food item was present but almost invisible.

**Cause:** there was a color code named --line in the parent block.

**Fix:** wrote a ui matching color orange in css of dish name and price which overrule the parent block command

**Checked:** dish price and name is now properly visible with matching ui

**Time:** took about 15 mins to find the color and css command



## CC-04 — "The buttons don't work on my tablet"
**Reproduced**: switch to ipad mini using dev tools on gogogle rowser tried to click on button and was not working

**Cause**: there was a transparent block over the buttons in img-wrap in tablet media which changed its color to black and removed transparency then it was visible. it happened in tablet only 
becoz that class was defind in the media of tablet specifically.

**Fix**:i searched that class name in all files no where used except for that block so removed that whole patch name .img-wrap::after

**Checked**: then loaded the site and it was working,
**Time**: 38 min ,first i checked the button was being clicked or not then moved to css debugging.



CC-05 — "The category bar scrolls away on my phone"
Reproduced: went to dev tools changed the screen size saw a bit of filter coming scroll concluded it to be becoz of padding and gaps

Cause: the section was not divided into parts and scroll was considering them as a whole block.

Fix: used flex box made vertical columns , made filter with fixed postion then the issue occure that sides of filter was not getting covered so i used width = 100% adn used overflow in horizontal direction to sort any issue with clipping

Checked: the screen scroll down and filter coming down as well

Time: 1 hr and 8 mins




## Could not fix

For anything you investigated but did not solve. Say what you tried and
where you got to. This is worth marks — leaving it blank when you got
stuck is not.

### CC-0X — "<the complaint>"

**What I tried:**

**Where I got to:**

**What I would try next:**



## Extra credit

Anything not on the bug log: a problem you found yourself, a test you
wrote, or a fix you are unsure about. Same format, plus one line on how
you noticed it.
