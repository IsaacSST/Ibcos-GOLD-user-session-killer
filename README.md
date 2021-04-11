# Automate Killing Sessions in Ibcos GOLD
Python script for killing idle gold sessions using root login through telnet connection with gold server.
Must enter gold server host addresss, login and password in corresponding variables in the script before using. Takes arguments auto and th. If auto argument is specified then the script will run automatically at a specified interval instead of just once. e.g auto:30 would run the script at 30 minute intervals. By default the script will kill all sessions idle for an hour or more, however using the 'th' argument one can specify a threshold of some amount of minutes less than an hour, e.g th:45 would kill sessions idle for 45 minutes or more. So examples could be 'Python kill.py auto:30' which would kill all sessions idle for an hour or more every 30 minutes, or 'Python kill.py auto:1 th:50' which would kill all sessions idle for 50 minutes or more every minute, i.e functioning more like a time-out for gold sessions. 'Python kill.py' will kill all sessions idle for over an hour, and not repeat. Note the script will always kill sessions idle for an hour or more, even if threshold is specified as a number of minutes more than an hour.
