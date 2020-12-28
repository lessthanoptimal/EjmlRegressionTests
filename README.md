hile EJML main repository includes regression tests, it does not have all the system specific hooks to automatically
update, run, and distribute the results. That's where this repository comes in.

# Set up

## Cron

In Linux, to run the regression test periodically you can use the crontab. Open the crontab with "crontab -e"
command then end the line at the bottom. It will run the task at noon on Tuesday and Friday. Output will
be saved to USER's home directory.

```commandline
00 12 * * 2,5 export PATH="/path/to/JRE/bin:$PATH";/usr/bin/python3 /home/USER/EjmlRegressionTests/cronscript.py > /home/USER/cron_output_ejml.log 2>&1
