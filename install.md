# tutorial
    https://www.stetic.com/developer/cronjob-linux-tutorial-und-crontab-syntax/
    https://www.youtube.com/watch?v=QZJ1drMQz1A

    https://vietnix.vn/crontab/

# crontab -l
    => listen crontab
# crontab -e
    => start und edit
# crontab -r
    => delete crontab

    
#  crontab mit generator
    https://crontab-generator.org/

# alle 5 minute
    */5 * * * *

# Structure
    # ┬ ───────────────  Minute (0-59)
    # | ┬ ─────────────  Stunde (0-23)  
    # │ │ ┬ ───────────  Tag (1-31) 
    # │ │ │ ┬ ─────────  Monat (1-12)
    # │ │ │ | ┬ ───────  day of week (0-6, Sonntag = 0 or 7)
    # │ │ | | | ┬ ─────  command to execute
    # │ | | | | |
    # 1 2 3 4 5 6
    # * * * * * command to execute

    example
    * * * * * echo "write text to file" >> /tmp/test.txt

* * * * * php /Users/nguyenle/Desktop/Developments/codes/Laravel/01-sources/cron_job/artisan schedule:run >> /dev/null 2>&1


# /etc/cron* Verzeichnisse
    /etc/cron.d/        =>  Erweiterungen zur /etc/crontab-Datei, gleiche Syntax.
    /etc/cron.daily/    =>  Einmal irgendwann täglich.
    /etc/cron.hourly/   =>  Einmal irgendwann stündlich.
    /etc/cron.monthly/  =>  Einmal irgendwann monatlich.
    /etc/cron.weekly/   =>  Einmal irgendwann wöchentlich.