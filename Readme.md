## Year long goals
- Create a cross platform application (Android and Web)
- Create an open source project
- Contribute to an open source project
- Continue and improve personal blog

## This week
- [x] Setup computer for React native development
- [ ] Build a simple React native app for Android
- [ ] Create same app in the web reusing as much code a possible
- [x] Investigate what is needed for a IOS emulator to run apps
- [ ] Create same app for IOS reusing as much code a possible
- [x] Ensure grive daemon is setup properly on my computer
- [x] Ensure github backup daemon is setup properly on my computer

## Week in review
To create IOS apps and run them, Mac OS X is required. This means
either a Mac computer or virtual machine is needed along with a
valid OS which requires a purchase. For now I am going to avoid
IOS apps since I don't really want to purchase Mac OS X.

## Learned this week
How to test a cron job
- `sudo crontab -e` to open crontab
- change cron job to run hourly and on an upcoming minute `01 * * * * CMD`
- `tail -f /var/log/syslog | grep CRON` to ensure that a the cron job runs
- If you do not have a mail server setup and the cron job produces output then the following
error occurs `CRON[8380]: (CRON) info (No MTA installed, discarding output)`
- Setup a main server `sudo apt-get install postfix`, choose Local, and output
will be sent to `/var/mail/root`

## Games of the week
- Sherlock Holmes: Crimes & Punishments
