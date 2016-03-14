# page-monitor-sample
sample of pmui

## Usage

1. install
2. launch web ui
3. collect pages

### Install

```sh
% git clone [this-repo-url]
% cd page-monitor-sample
% npm i
# if needs
% npm i phantomjs -g 
```

### Launch web UI

Select each tool you need.

- node (development)
- [PM2 - Advanced Node.js process manager](http://pm2.keymetrics.io/)
- [forever](https://github.com/foreverjs/forever)

#### launch ui server by node (development)

```sh
% node app.js
```

#### launch ui server by PM2

```sh
% pm2 start app.js --name pmui
```

#### launch ui server by 

```sh
% forever start app.js
```

### set collecting script

(create each site script like `www.google.com.js`)

collect diffs of google.com each 60 seconds.

use forever or crontab etc.

```sh
% forever start --spinSleepTime 60000 www.google.com.js
```

### view difference in browser

access http://localhost:8894/
