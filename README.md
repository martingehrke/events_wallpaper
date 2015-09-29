Brief undetailed write up

This script uses IFTTT (AKA IF) to change the wallpaper of your android device based on the day and a couple files.

**USES**
* set your wallpaper to your favorite football teams on gameday
* set your wallpaper on your REDDIT cakeday
* " for your wedding
* last day of school
* first day of school
* days you are on support

**FILES:**
* change | this needs to run once a day  
* random | list of random image URLs in case there is no match  
* events | list of dates in YYYYMMDD format with a space then a URL  
* crontab.example | edit this to add the right path to change and load with crontab ./crontab.example

change runs once a day and matches a line in the events file. it then posts the url to IFTTT which will update the background of your cellphone.

**LOOSE ENDS:**
I will try to publish my recipe in the near future.  
You need to create a recipe of the MAKER type at https://ifttt.com/maker with the event_name of change_wallpaper. It then needs to take the url in value1 to update your android wallpaper.

You need to create a cron job that runs probably first thing in the morning 1AM or so, when you are sleeping but have wifi on.

You need to have the ifttt android app on your phone so it can change the background.

**TODO:**
* move ifttt api key to separate file
* use proper flags for options
* handle duplicate dates sanely, instead of ignoring 
* remove past dates from file
* support for repeating yearly entries (MMDD)
