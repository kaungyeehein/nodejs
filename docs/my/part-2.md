# ကိုကောင်း၏ NodeJS မှတ်စု

Language: MY|[EN](../en/part-2.md)

## မာတိကာ

### 📒 အပိုင်း (၁)

* [(၁) NodeJS မိတ်ဆက်](./index.md#၁-nodejs-မိတ်ဆက်)
* [(၂) NodeJS ကိုထည့်သွင်းခြင်း](./index.md#၂-nodejs-ကိုထည့်သွင်းခြင်း)
* [(၃) Project Directory ပြုလုပ်ခြင်း](./index.md#၃-project-directory-ပြုလုပ်ခြင်း)
* [(၄) VSCode အသုံးပြုခြင်း](./index.md#၄-vscode-အသုံးပြုခြင်း)
* [(၅) ClientJS Env နှင့် NodeJS Env](./index.md#၅-clientjs-env-နှင့်-nodejs-env)
* [(၆) NodeJS အခြေခံ](./index.md#၆-nodejs-အခြေခံ)
* [(၇) Module များခွဲထုတ်ရေးသားခြင်း](./index.md#၇-module-များခွဲထုတ်ရေးသားခြင်း)

### 📒 အပိုင်း (၂)

* [(၈) ExpressJS ထည့်သွင်းခြင်း](./part-2.md#၈-expressjs-ထည့်သွင်းခြင်း)
* [(၉) View Engine အသုံးပြုခြင်း](./part-2.md#၉-view-engine-အသုံးပြုခြင်း)
* [(၁၀) Session](./part-2.md#)

[👆 မာတိကာသို့](#မာတိကာ)

---

## ~~~ 📒 အပိုင်း (၂) ~~~

### (၈) ExpressJS ထည့်သွင်းခြင်း

NodeJS ကိုအသုံးပြုပြီး web application တစ်ခုပြုလုပ်မည် ဆိုပါက http module ကိုအသုံးပြုပြီး web server ပြုလုပ်ကာ application အတွက်လိုသည်များကို အသေးစိတ်ပြုလုပ်နိုင်ပါသည်။ သို့သော်လည်း ထိုကဲ့သို့ အသေးစိတ် low level အထိလိုက်ရေးမနေဘဲ အသင့်ပြုလုပ်ထားသော framework များကို အသုံးပြုကား လွယ်ကူလျှင်မြန်စွာ application များကို တည်ဆောက်နိုင်မှာ ဖြစ်ပါသည်။ ထိုသို့ပြုလုပ်ရာတွင် web application များအတွက် လူသုံးများပြီး၊ အလွန်အသုံးဝင်သော framework တစ်ခုမှာ ExpressJS ပင်ဖြစ်ပါသည်။ ExpressJS ကိုထည့်သွင်းရန် project directory ထဲတွင် အောက်ပါအတိုင်း terminal မှရိုက်၍ install ပြုလုပ်ပါမည်။
```
npm i express
```
Install ပြုလုပ်ပြီးပါက `package.json` file ထဲရှိ dependencies အောက်တွင် install ပြုလုပ်ထားသော ExpressJS ၏ version အားတွေ့ရမည် ဖြစ်ပါသည်။ ထိုနောက် application အား စတင်ရေးသားရန် terminal ထဲတွင် `code .` ဟုရိုက်၍ VSCode အားဖွင့်ပါမည်။ index file အားပြုလုပ်ရန် terminal ထဲတွင် `touch index.js` ဟုရိုက်ပါသည်။ ထိုနောက် အောက်ပါအတိုင်း index.js အား VSCode ထဲတွင် ရေးပါမည်။
```javascript
// index.js
const express = require('express');

const app = express();

app.get('/', (req, res, next) => {
    res.send('Hello World!');
});

app.listen(3000);
```
၎င်း application ကို run ရန် terminal ထဲတွင် `node index.js` ဟုရိုက်ထည့်ပြီး၊ web browser ကနေ `http://localhost:3000` ဟုရှာကြည့်ပါက 'Hello World!' ဟူသော ပထမဦးဆုံး application စမ်းသပ်တာကို မြင်ရမှ ဖြစ်ပါသည်။ Project ထဲတွင် install ပြုလုပ်ထားသော ExpressJS အား index.js ၏ ပထမဦးဆုံး စာကြောင်းတွင် require ပြုလုပ်ထားသည်မှာ ၎င်း module အား import ပြုလုပ်ထားခြင်း ဖြစ်ပါသည်။ ထိုနောက် express application အား initalize ပြုလုပ်ထားပါသည်။ application ၏ root အားခေါ်ပါက အလုပ်လုပ်မည့် callback function အားရေးထားပြီး၊ ၎င်း callback ထဲတွင် request, response နဲ့ next ဟူသော parameter များလက်ခံ ဆောင်ရွက်ထားသည်ကို တွေ့ရမည် ဖြစ်ပါသည်။ နောက်ဆုံးတွင် port အမှတ် 3000 တွင် application အားလက်ခံ ဆောင်ရွက်မည် ဟု ကြေညှာထားခြင်း ဖြစ်ပါသည်။

NodeJS application ၏ `index.js` တွင် တစ်ခုခုပြောင်းလဲချင်ပါက NodeJS application ကို ရပ်၍ ပြန်လည်စတင်ရပါသည်။ ထိုအရာကို အလိုအလျှောက် ပြုလုပ်လိုပါက နောက်ထပ် မဖြစ်မနေ ထည့်သွင်းသင့်တဲ့ module ကတော့ `nodemon` ဖြစ်ပါတယ်။ `nodemon` ကိုထည့်သွင်းရန် terminal ထဲတွင် အောက်ပါအတိုင်း ရိုက်ထည့်ပါ။
```
npm i -D nodemon
```
ExpressJS သွင်းတုန်းကနှင့် မတူသည်မှာ -D ထည့်ထားခြင်းဖြစ်သည်။ `nodemon` သည် development ပြုလုပ်ချိန် အတွက်သာ လိုအပ်သောကြောင့်ဖြစ်ပါသည်။ `package.json` file ထဲရှိ devDependencies အောက်တွင် nodemon ရောက်ရှိနေမည်ဖြစ်ပါသည်။ `package.json` ၏ `scripts` တွင်လည်း `nodemon` ကိုအသုံးပြုရန် အောက်ပါအတိုင် ပြောင်းလည်း ရေးသားရမည် ဖြစ်ပါသည်။
```
"scripts": {
    "start": "nodemon index.js"
  }
```
Application ကို စမ်းကြည့်ရန် terminal တွင် `npm start` ဟုရိုက်ထည့်ပါက `nodemon` ကိုမြင်ရမည် ဖြစ်ပြီး၊ JavaScript file တွင် တစ်ခုခု အပြောင်းအလဲ လုပ်ပါက application အား auto restart ပြုလုပ်သွားမည် ဖြစ်ပါသည်။

[👆 မာတိကာသို့](#မာတိကာ)

---

### (၉) View Engine အသုံးပြုခြင်း

MVC Pattern များအသုံးပြု၍ Application များရေးသားရာတွင် HTML code များတွင် view နှင့် data ကို ခွဲထုတ်၍ ရေးသားလေ့ရှိကြပါသည်။ ထို့သို့ရေးသားရာတွင် အသုံးပြုနိုင်သော Template Engine များ များစွာရှိသည့်အနက် EJS နှင့် Pug ကို အရင် လေ့လာရန် တိုက်တွန်းပါသည်။ ထိုနောက် မိမိအားသာရာ ရေးထုံးကို အသုံးပြု ရေးသားနိုင်ပါသည်။

#### EJS

EJS ၏ ရေးပုံရေးနည်းမှာ HTML များအတိုင်းပင် ဖြစ်ပါသည်။ Default အနေနှင့် percentage tag <% %> များအတွင်း EJS များကို ထည့်သွင်း ရေးသား သွားခြင်းဖြစ်သောကြောင့် အထူတလည် လေ့လာရန်မလိုပဲ လေ့လာရလွယ်ကူပါသည်။ Express v4 မှစတင်က EJS ကို လွယ်ကူစွာ ထည့်သွင်း အသုံးပြုနိုင်ပါသည်။ EJS ကိုထည့်သွင်းရန် Terminal ထဲတွင် အောက်ပါအတိုင်း EJS Package ကိုထည့်သွင်းပါ။
```
npm i ejs
```
ထိုနောက် အောက်ပါနာမူနာ အတိုင်း `app.js` ကို ရေးသားပါ။
```javascript
// app.js
const express = require('express');
const app = express();

app.set('view engine', 'ejs');

app.get('/', (req, res) => {
  res.render('home', {name: 'Kaung'});
});

app.listen(3000, () => console.log('App listening on port 3000!'));
```
View များထည့်သွင်းရန် `mkdir views` command ဖြင့် `views` ဟူသော directory တစ်ခုပြုလုပ်၍ ၎င်းထဲတွင် `home.ejs` file တစ်ခုကို အောက်ပါအတိုင်း ရေးထည့်ပါ။ Directory name ကို `views` ဟုမပေးဘဲ ကြိုက်နှစ်သက်ရာ နာမည်ပေးနိုင်ပါသည်။ ထိုသို့ပြုလုပ်လိုပါက `app.set('views', path.join(__dirname, 'views'));` ဖြင့် ကြေညှာပေးရမှာ ဖြစ်ပါသည်။ 
```ejs
// views/home.ejs
<h1>
Hello, <%= name %>
</h1>
```
၎င်း application ကို run ကြည့်ပါက Hello, Kaung ဟူသော စာမျက်နှာအား မြင်ရမည် ဖြစ်ပါသည်။ EJS ရေးထုံးများကို အသေးစိတ်လေ့လာလိုပါက [EJS(Github)](https://github.com/mde/ejs/blob/master/docs/syntax.md) တွင် လေ့လာနိုင်ပါသည်။ VSCode တွင် EJS များကို syntax highlight ပြုလုပ်လိုပါက `EJS language support` extension ကိုထည့်သွင်း အသုံးပြုနိုင်ပါသည်။ ထိုအခါ VSCode ထဲတွင် ejs ဟုရိုက်၍ template များကိုပါ ခေါ်ယူအသုံးပြုနိုင်မှာ ဖြစ်ပါသည်။

EJS စာမျက်နှာများကို layout တစ်ခုထဲပေါ်တွင် ပုံစံတစ်ကျ ဖြစ်လိုပါက `express-ejs-layouts` package ကို ထည့်သွင်း အသုံးပြုရမည် ဖြစ်ပါသည်။ ၎င်းကို ထည့်သွင်းရန် အောက်ပါတိုင်း console တွင် ရိုက်ထည့်ပါ။
```
npm i express-ejs-layouts
```
Layouts package ကို ထည့်သွင်းပြီးပါက `app.js` တွင် `const expressLayouts = require('express-ejs-layouts')` ကိုထည့်သွင်းပြီး `app.use(expressLayouts);` ဖြင့် အသုံးပြုပေးရမည် ဖြစ်ပါသည်။ ထိုနောက် `layout.ejs` file အား views directory ထဲတွင် အောက်ပါအတိုင်း ပြုလုပ်ပါ။
```ejs
// views/layout.ejs
<!DOCTYPE html>
<html>
    <head>
        <meta charset="utf-8">
        <title>EJS Layout</title>
    </head>
    <body>
        <h1>This is in the layout file.</h1>
        <%- include('common/header') %>
        <%- body %>
        <%- include('common/footer') %>
    </body>
</html>
```
၎င်း layout ဖြင့် မည်သည့် EJS စာမျက်နှာများကိုမဆို ဖေါ်ပြပေးမည်ဖြစ်ပြီး၊ `<%- body %>` နေရာတွင် ခေါ်လိုက်သော EJS စာမျက်နှာ ဝင်ရောက်လာမည် ဖြစ်ပါသည်။ နောက်ထပ်ပြောပြ လိုသည်မှာ EJS စာမျက်နှာ များတွင် တူညီသော အကြောင်းအရာများ common များကို ခွဲထုတ်ရေးသား၍ ပြန်လည်အသုံးပြုနိုင်ပါသည်။ အထက်ပါ `layout.ejs` တွင် တူညီသော Header နှင့် Footer ကို views အောက်ရှိ common ဟူသော directory ထဲတွင် ခွဲထုတ်ရေးသားထားကာ include ဖြင့် ပြန်လည်ခေါ်ယူထားခြင်း ဖြစ်ပါသည်။

#### Pug

Pug သည် template engine တစ်ခုဖြစ်သည်။ ရေးထုံးရေးနည်းသည် ejs နဲ့အတူပဲ ကွဲပြားပါသည်။ ရေးသားပုံမှာ tab များ၊ space များ၊ new line များကို အသုံးပြုကာ structure တည်ဆောက်၍ ရေးသားရသော language ဖြစ်ပါသည်။ Pug ကိုထည့်သွင်းရန် Terminal ထဲတွင် အောက်ပါအတိုင်း Pug Package ကိုထည့်သွင်းပါ။
```
npm i pug
```
ထိုနောက် အောက်ပါနာမူနာ အတိုင်း `app.js` ကို ရေးသားပါ။ `app.js` တွင် EJS နှင့်ကွာခြားသွားသည်မှာ view engine တွင် ejs အစား pug ဖြစ်သွားခြင်းဖြစ်သည်။
```javascript
// app.js
const express = require('express');
const app = express();

app.set('view engine', 'pug');

app.get('/', (req, res) => {
  res.render('home', {name: 'Kaung'});
});

app.listen(3000, () => console.log('App listening on port 3000!'));
```
View များထည့်သွင်းရန် `mkdir views` command ဖြင့် `views` ဟူသော directory တစ်ခုပြုလုပ်၍ ၎င်းထဲတွင် `home.pug` file တစ်ခုကို အောက်ပါအတိုင်း ရေးထည့်ပါ။ Directory name ကို `views` ဟုမပေးဘဲ EJS မှာလို ကြိုက်နှစ်သက်ရာ နာမည်ပေးနိုင်ပါသည်။
```pug
// views/home.pug
h1 Hello, #{name}
```
၎င်း application ကို run ကြည့်ပါက Hello, Kaung ဟူသော စာမျက်နှာအား မြင်ရမည် ဖြစ်ပါသည်။ Pug ရေးထုံးများကို အသေးစိတ်လေ့လာလိုပါက [pugjs.org (Language Reference)](https://pugjs.org/language/doctype.html) တွင် လေ့လာနိုင်ပါသည်။ ၎င်းတွင် Attributes, Case, Code, Comments, Conditionals, Doctype, Filters, Includes, Iteration, Mixins စသည်ဖြင့် လေ့လာစရာ ရေးပုံရေးနည်းများစွာ ရှိပါသည်။ Pug ၏ အဓိကအားသာချက်မှာ code အနည်းငယ်ရေးသားယုံဖြင့် HTML code များကို ပြည့်ပြည့်စုံစုံ ဖေါ်ပြပေးနိုင်ခြင်း ဖြစ်ပါသည်။ EJS မှာလို HTML code များကို အကုန်ရေးသားစရာ မလိုပဲ Pug က ၎င်း၏ template များကို အသုံးပြုကာ ဖေါ်ပြပေးသွားမှာ ဖြစ်ပါသည်။ ထိုအပြင် EJS မှာလိုပင် တူညီသော Header နှင့် Footer ကို views အောက်ရှိ common ဟူသော directory ထဲတွင် ခွဲထုတ်ရေးသားထားကာ include ဖြင့် ပြန်လည်ခေါ်ယူ ထားနိုင်ပါသည်။ အောက်ပါ code နမူနာကို ကြည့်ပါ။
```pug
// views/home.pug
doctype html
html
    head
        title Pug Layout
    body
        include common/header
        h1 Hello, #{name}
        include common/footer
```
ထိုကဲ့သို့ Pug အားအသုံးပြုကာ ရေးသားပါက အောက်ပါအတိုင်း HTML code ထွက်လာမှာ ဖြစ်ပါတယ်။ တိုတောင်းပြီး ကျစ်လစ်သော code ရေးထုံးရေးနည်းများကြောင့် Pug အား လူကြိုက်များလှခြင်း ဖြစ်ပါသည်။ အားနည်းချက်မှာ ရေးထုံးရေးနည်းများကို အသစ်ပြန်လည် လေ့လာရခြင်းဖြစ်ပါသည်။
```html
<!DOCTYPE html>
<html>
    <head>
        <title>Pug Layout</title>
    </head>
    <body>
        <header>This is header</header>
        <h1>Hello, Kaung</h1>
        <footer>This is footer</footer>
    </body>
</html>
```

[👆 မာတိကာသို့](#မာတိကာ)

---
