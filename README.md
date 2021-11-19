# **WebsDB** : The webscraper on JobsDb

---
> using just BeautifulSoup & Requests Packages (No Selenium needed)
<img src="https://github.com/wallik2/Jobsdb_WebScraper/blob/main/picture/JobsDB_meme.jpg?raw=true" width="50%">

[![open in colab](https://camo.githubusercontent.com/52feade06f2fecbf006889a904d221e6a730c194/68747470733a2f2f636f6c61622e72657365617263682e676f6f676c652e636f6d2f6173736574732f636f6c61622d62616467652e737667)](https://colab.research.google.com/drive/1J-7DNtrsZj8nN2YhD9g-hypexiVO4mI_?usp=sharing)

--- 
## Brief summary

- 

[![Build Status](https://travis-ci.org/joemccann/dillinger.svg?branch=master)](https://travis-ci.org/joemccann/dillinger)

Dillinger is a cloud-enabled, mobile-ready, offline-storage compatible,
AngularJS-powered HTML5 Markdown editor.

- Type some Markdown on the left
- See HTML in the right
- Suppose we scraped the data given **'doctor'** as keyword 

|index|job title                                                                                                        |more info                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |job_company                                        |job_location              |skill requirement 1                               |skill requirement 2                               |skill requirement 3                               |posted time|
|------|-----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------|--------------------------|--------------------------------------------------|--------------------------------------------------|--------------------------------------------------|-----------|
|0     |Medical Doctor                                                                                                   |https://th.jobsdb.com//th/en/job/medical-doctor-300003002466359?token=0~426b9c9f-ab6e-4fae-aaa8-168612118aa6&sectionRank=1&jobId=jobsdb-th-job-300003002466359                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |Minor Hotel Group Limited                          |Petchaburi                |Bachelor of Medicine                              |5 to 7 yrs of clinical experience                 |Doctor of Medicine                                |5d ago     |
|1     |Nurse (Telemedicine)                                                                                             |https://th.jobsdb.com//th/en/job/nurse-telemedicine-300003002461247?token=0~426b9c9f-ab6e-4fae-aaa8-168612118aa6&sectionRank=2&jobId=jobsdb-th-job-300003002461247                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |Good Doctor Technology (Singapore) Pte Ltd.        |Pathumwan                 |                                                  |                                                  |                                                  |20h ago    |
|2     |HR staff (HRD Department)(ID:60722)                                                                              |https://th.jobsdb.com//th/en/job/hr-staff-hrd-department-id%3A60722-300003002470542?token=0~426b9c9f-ab6e-4fae-aaa8-168612118aa6&sectionRank=3&jobId=jobsdb-th-job-300003002470542                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |Reeracoen Recruitment Co., Ltd.                    |Wattana                   |Bachelor degree in any fields                     |Good command in English                           |New Graduated                                     |20h ago    |
|3     |แม็คโคร สาขาบางคอแหลม (เจริญกรุง 109) เปิดรับสมัคร พนักงานส่วนซ่อมบำรุง (Staff - General Affair)                 |https://th.jobsdb.com//th/en/job/%E0%B9%81%E0%B8%A1%E0%B9%87%E0%B8%84%E0%B9%82%E0%B8%84%E0%B8%A3-%E0%B8%AA%E0%B8%B2%E0%B8%82%E0%B8%B2%E0%B8%9A%E0%B8%B2%E0%B8%87%E0%B8%84%E0%B8%AD%E0%B9%81%E0%B8%AB%E0%B8%A5%E0%B8%A1-%E0%B9%80%E0%B8%88%E0%B8%A3%E0%B8%B4%E0%B8%8D%E0%B8%81%E0%B8%A3%E0%B8%B8%E0%B8%87-109-%E0%B9%80%E0%B8%9B%E0%B8%B4%E0%B8%94%E0%B8%A3%E0%B8%B1%E0%B8%9A%E0%B8%AA%E0%B8%A1%E0%B8%B1%E0%B8%84%E0%B8%A3-%E0%B8%9E%E0%B8%99%E0%B8%B1%E0%B8%81%E0%B8%87%E0%B8%B2%E0%B8%99%E0%B8%AA%E0%B9%88%E0%B8%A7%E0%B8%99%E0%B8%8B%E0%B9%88%E0%B8%AD%E0%B8%A1%E0%B8%9A%E0%B8%B3%E0%B8%A3%E0%B8%B8%E0%B8%87-staff-general-affair-300003002459826?token=0~426b9c9f-ab6e-4fae-aaa8-168612118aa6&sectionRank=4&jobId=jobsdb-th-job-300003002459826                                                                                                                                                                                                                           |Siam Makro Public Company Limited                  |Bangkor-laem              |                                                  |                                                  |                                                  |2d ago     |
|4     |Accountant/เจ้าหน้าที่บัญชี                                                                                      |https://th.jobsdb.com//th/en/job/accountant-%E0%B9%80%E0%B8%88%E0%B9%89%E0%B8%B2%E0%B8%AB%E0%B8%99%E0%B9%89%E0%B8%B2%E0%B8%97%E0%B8%B5%E0%B9%88%E0%B8%9A%E0%B8%B1%E0%B8%8D%E0%B8%8A%E0%B8%B5-300003002466185?token=0~426b9c9f-ab6e-4fae-aaa8-168612118aa6&sectionRank=5&jobId=jobsdb-th-job-300003002466185                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |GCC Services (Thailand) Co., Ltd.                  |Sathorn                   |                                                  |                                                  |                                                  |20h ago    |

scraped at 19/11/64 20:15 


<font size="7"> There are 8 features that it scrapes. </font>

## How it works 
<img src="https://github.com/wallik2/Jobsdb_WebScraper/blob/main/picture/1.search_jobsdb.png?raw=true" >

## Features

- Import a HTML file and watch it magically convert to Markdown
- Drag and drop images (requires your Dropbox account be linked)
- Import and save files from GitHub, Dropbox, Google Drive and One Drive
- Drag and drop markdown and HTML files into Dillinger
- Export documents as Markdown, HTML and PDF

Markdown is a lightweight markup language based on the formatting conventions
that people naturally use in email.
As [John Gruber] writes on the [Markdown site][df1]

> The overriding design goal for Markdown's
> formatting syntax is to make it as readable
> as possible. The idea is that a
> Markdown-formatted document should be
> publishable as-is, as plain text, without
> looking like it's been marked up with tags
> or formatting instructions.

This text you see here is *actually- written in Markdown! To get a feel
for Markdown's syntax, type some text into the left window and
watch the results in the right.

## Tech

Dillinger uses a number of open source projects to work properly:

- [AngularJS] - HTML enhanced for web apps!
- [Ace Editor] - awesome web-based text editor
- [markdown-it] - Markdown parser done right. Fast and easy to extend.
- [Twitter Bootstrap] - great UI boilerplate for modern web apps
- [node.js] - evented I/O for the backend
- [Express] - fast node.js network app framework [@tjholowaychuk]
- [Gulp] - the streaming build system
- [Breakdance](https://breakdance.github.io/breakdance/) - HTML
to Markdown converter
- [jQuery] - duh

And of course Dillinger itself is open source with a [public repository][dill]
 on GitHub.

## Installation

Dillinger requires [Node.js](https://nodejs.org/) v10+ to run.

Install the dependencies and devDependencies and start the server.

```sh
cd dillinger
npm i
node app
```

For production environments...

```sh
npm install --production
NODE_ENV=production node app
```

## Plugins

Dillinger is currently extended with the following plugins.
Instructions on how to use them in your own application are linked below.

| Plugin | README |
| ------ | ------ |
| Dropbox | [plugins/dropbox/README.md][PlDb] |
| GitHub | [plugins/github/README.md][PlGh] |
| Google Drive | [plugins/googledrive/README.md][PlGd] |
| OneDrive | [plugins/onedrive/README.md][PlOd] |
| Medium | [plugins/medium/README.md][PlMe] |
| Google Analytics | [plugins/googleanalytics/README.md][PlGa] |

## Development

Want to contribute? Great!

Dillinger uses Gulp + Webpack for fast developing.
Make a change in your file and instantaneously see your updates!

Open your favorite Terminal and run these commands.

First Tab:

```sh
node app
```

Second Tab:

```sh
gulp watch
```

(optional) Third:

```sh
karma test
```

#### Building for source

For production release:

```sh
gulp build --prod
```

Generating pre-built zip archives for distribution:

```sh
gulp build dist --prod
```

## Docker

Dillinger is very easy to install and deploy in a Docker container.

By default, the Docker will expose port 8080, so change this within the
Dockerfile if necessary. When ready, simply use the Dockerfile to
build the image.

```sh
cd dillinger
docker build -t <youruser>/dillinger:${package.json.version} .
```

This will create the dillinger image and pull in the necessary dependencies.
Be sure to swap out `${package.json.version}` with the actual
version of Dillinger.

Once done, run the Docker image and map the port to whatever you wish on
your host. In this example, we simply map port 8000 of the host to
port 8080 of the Docker (or whatever port was exposed in the Dockerfile):

```sh
docker run -d -p 8000:8080 --restart=always --cap-add=SYS_ADMIN --name=dillinger <youruser>/dillinger:${package.json.version}
```

> Note: `--capt-add=SYS-ADMIN` is required for PDF rendering.

Verify the deployment by navigating to your server address in
your preferred browser.

```sh
127.0.0.1:8000
```

## License

MIT

**Free Software, Hell Yeah!**

[//]: # (These are reference links used in the body of this note and get stripped out when the markdown processor does its job. There is no need to format nicely because it shouldn't be seen. Thanks SO - http://stackoverflow.com/questions/4823468/store-comments-in-markdown-syntax)

   [dill]: <https://github.com/joemccann/dillinger>
   [git-repo-url]: <https://github.com/joemccann/dillinger.git>
   [john gruber]: <http://daringfireball.net>
   [df1]: <http://daringfireball.net/projects/markdown/>
   [markdown-it]: <https://github.com/markdown-it/markdown-it>
   [Ace Editor]: <http://ace.ajax.org>
   [node.js]: <http://nodejs.org>
   [Twitter Bootstrap]: <http://twitter.github.com/bootstrap/>
   [jQuery]: <http://jquery.com>
   [@tjholowaychuk]: <http://twitter.com/tjholowaychuk>
   [express]: <http://expressjs.com>
   [AngularJS]: <http://angularjs.org>
   [Gulp]: <http://gulpjs.com>

   [PlDb]: <https://github.com/joemccann/dillinger/tree/master/plugins/dropbox/README.md>
   [PlGh]: <https://github.com/joemccann/dillinger/tree/master/plugins/github/README.md>
   [PlGd]: <https://github.com/joemccann/dillinger/tree/master/plugins/googledrive/README.md>
   [PlOd]: <https://github.com/joemccann/dillinger/tree/master/plugins/onedrive/README.md>
   [PlMe]: <https://github.com/joemccann/dillinger/tree/master/plugins/medium/README.md>
   [PlGa]: <https://github.com/RahulHP/dillinger/blob/master/plugins/googleanalytics/README.md>
