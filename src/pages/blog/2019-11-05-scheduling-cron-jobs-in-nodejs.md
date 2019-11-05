---
templateKey: blog-post
title: Scheduling Cron Jobs in NodeJS
date: 2019-11-05T23:24:08.767Z
description: >-
  The software utility cron is a time-based job scheduler in Unix-like computer
  operating systems. Users that set up and maintain software environments use
  cron to schedule jobs to run periodically at fixed times, dates, or intervals
featuredpost: true
featuredimage: /img/cron.png
tags:
  - cron
  - node
  - react
  - material-ui
  - script
---
!\[script-clock](/img/cron.png)

\## Getting started

\`\`\`npm i --save cron\`\`\`

\# 

\#### Creating a cron job

\`\``const CronJob = require('cron').CronJobconst onCronTick = () => console.log('Cron Job Running')

new CronJob({    onTick: onCronTick,    start: true,    timeZone: 'America/New_York',    cronTime: '0 30 9 \* \* MON'})\`\``

Lets go through the four properties we set in the cron job

\##### 

\* \*\*onTick      -\*\* This is the function that execute when the cron job runs\* \*\*start         -\*\* Tell the cron job to start when instantiated\* \*\*timeZone -\*\* Timezone you would like the cron job execute based off\* \*\*cronTime -\*\* This string of data is known as the "cron expression". This tells the cron job when exactly to execute

\### Creating a cron expression`<second> <minute> <hour> <day-of-month> <month> <day-of-week> <year(optional)>`  Above is a cron expression in terms of value placement. In our code example of the cron job, the expression reads "Execute at 09:30 AM, only on Monday"

\### React Cron GeneratorYou can also use a generator to create these expressions for you  \[Live demo](https://dealmeddevs.github.io/react-cron-generator/)



\> NOTE: This cron library does support seconds. However many linux machines dont  > To learn more about cron expressions, \[ see oracle docs](https://docs.oracle.com/cd/E12058_01/doc/doc.1014/e12030/cron_expressions.htm)
