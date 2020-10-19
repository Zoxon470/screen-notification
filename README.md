# A script to remind you of the time log
Good afternoon, ladies and gentlemen. From time to time I forget to log the time, so I wanted to use some software that reminds me of this with the messages "LOG TIME". But alas, I did not find a suitable software for macOS, and somehow it was necessary to solve the problem.

[![Screen_Shot_2018-08-21_at_9.30.02_AM.png](https://i.postimg.cc/hGQ33X7p/Screen-Shot-2020-10-19-at-17-58-08.png)](https://postimg.cc/KKFN1vfM)

I offer you my solution.

##### For macOS:
1. Open a terminal and enter the following:
```sh
$ env EDITOR=nano crontab -e # We open it through `nano` so that it is not a problem to exit `vim`.
```
2. We enter the following:
```sh
$ 30 * * * * osascript -e 'display notification "Time to log time!!!!"'
```
3. We save this whole thing by combining the keys CONTROL + O
4. Now every 30 minutes we will be reminded to log our time.

#### Notes
* [Online cron job generator](https://crontab.guru/)
* [Documentation the osascript](https://ss64.com/osx/osascript.html)
