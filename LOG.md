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

CC-10: "Sorting by price is backwards"
Reproduced: Press filter changed to low to high and vice versa it was opposedly working

Cause: The logic for asc and dec was opposite the wrote

Fix: correct the logic

Checked:Checked the feature it is working now

Time: 43min majority of the time was tkaen to find the code coz i was search acc to id and function name and api stuff , then saw it in logic folder which token few seconds to change.

CC-09 — "The menu shows more dishes than it should"
Reproduced: scroll down again and again

Cause: there was infinite scroll written

Fix: commented it out

Checked: checked the site , it was loading more when the button is clicked 
Time: 50 min, took time to first find api,server then searched frontend then didnt expect the whole code to found so was founding in between as well, so took time

CC-06 — "I ordered more than they had"
Reproduced: ordered veg momos more that they had ,  inventory went into negative

Cause: in validation , there was no check related to over the stock problem

Fix: did 3 changes first to see in ui, second there was main logic in validation , and an internal server check present in smoke.js

Checked: order was not placed when i did with grilled sandwich having less stock than order

Time: approx 2hrs, first looked into frontend code found the bug , didnt work then searched for other backend and while finding it i did it in smoke and then validation file


CC-07: "Cancelling makes it worse"
Reproduced: i treid cancelling first i thought it would be deducting but i was getting deducted twice the number we ordered

Cause: in the logic return statement - was used

Fix: changed - to + so that the order logic which had removed the stock by order api will add the number deducted.

Checked: tried canceled order and went to see in counter it worked.

Time:15min , majority of the time was to trace the function where logic was used.



CC-XX1 — "two local host same files but + button after add to cart button in menu page not working in one file"
What I tried: whn bug was found about + not working i tried to edit css file to which new code did it but cant find it so copy paste the css file edited one into new cloned repo ran in diffenrt port .

Where I got to: bug was not solved

What I would try next: happened first time with me and no ai is allowed so dont know what to do.


CC-0X — "quantity in main screen of menu is slightly visible"
Reproduced: clicked add to cart , quantity number was almost invisible

Cause: color was used from parent which is --line color

Fix: change the color to white or --ink

Checked: rant he server and saw the quantity

Time:5 min (also to write to log)

CC-0X — "my order page not working"
What I tried: i tried to trace from frontend to backend.

Where I got to: got stuck on backend api file having /api/orders/:token 

What I would try next: i think that the order placed doesnt have or not gets an updated attribute which allow its if condition to work and show placed orders loaded orders

Bug Solved 
Cause : there was no userid in store json and memberid was compared with it
fix : did changes in comparison of memberid with memberid .
time (: 1hr looking somewhere else at the dedicated place for mmy orders :)



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
