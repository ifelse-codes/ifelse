---
title: "How to Save Web Page as Pdf in Node Js"
date: 2020-03-26T01:44:37+05:30
draft: false

---

We can use `puppeteer` to save any webpage as `pdf` file.

`puppeteer` is a node js library to work with `headless chrome`.


##### In this example we'll save content of [this post](https://ifelse.codes/how-to-save-web-page-as-pdf-in-node-js/) to disk. 

###### Step-1 Install puppeteer 
```
npm i puppeteer --save
```
This will install Puppeteer.
It downloads a recent version of Chromium that is guaranteed to work with the API. 

###### Step-2 Script To Save webpage as PDF file
```
const puppeteer = require('puppeteer'); 
(async () => {
  const browser = await puppeteer.launch();
  const page = await browser.newPage();
  await page.goto('https://ifelse.codes/how-to-save-web-page-as-pdf-in-node-js');
  await page.pdf({path: './ifelse_tutorials.pdf' , format: 'A4'});

  await browser.close();
})();
```
Save this this code as `to_pdf.js`
Execute the script on command line with 
```
node to_pdf.js
```