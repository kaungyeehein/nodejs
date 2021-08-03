# ကိုကောင်း၏ NodeJS မှတ်စု

Language: MY|[EN](../en/part-2.md)

## မာတိကာ

### 📒 အပိုင်း (၁)

1. [NodeJS မိတ်ဆက်](./index.md#၁-nodejs-မိတ်ဆက်)
2. [NodeJS ကိုထည့်သွင်းခြင်း](./index.md#၂-nodejs-ကိုထည့်သွင်းခြင်း)
3. [Project Directory ပြုလုပ်ခြင်း](./index.md#၃-project-directory-ပြုလုပ်ခြင်း)
4. [VSCode အသုံးပြုခြင်း](./index.md#၄-vscode-အသုံးပြုခြင်း)
5. [NodeJS အခြေခံ](./index.md#၅-nodejs-အခြေခံ)
6. [ClientJS Env နှင့် NodeJS Env](./index.md#၆-clientjs-env-နှင့်-nodejs-env)
7. [Module များခွဲထုတ်ရေးသားခြင်း](./index.md##၇-module-များခွဲထုတ်ရေးသားခြင်း)

### 📒 အပိုင်း (၂)

8. [ExpressJS ထည့်သွင်းခြင်း](./part-2.md#၈-expressjs-ထည့်သွင်းခြင်း)

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