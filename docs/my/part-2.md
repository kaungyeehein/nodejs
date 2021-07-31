# ကိုကောင်း၏ NodeJS မှတ်စု

Language: MY|[EN](../en/part-2.md)

## မာတိကာ

### 📒 အပိုင်း (၁)

* [(၁) NodeJS မိတ်ဆက်](./index.md#၁-nodejs-မိတ်ဆက်)
* [(၂) NodeJS ကိုထည့်သွင်းခြင်း](./index.md#၂-nodejs-ကိုထည့်သွင်းခြင်း)
* [(၃) Project Directory ပြုလုပ်ခြင်း](./index.md#၃-project-directory-ပြုလုပ်ခြင်း)
* [(၄) VSCode အသုံးပြုခြင်း](./index.md#၄-vscode-အသုံးပြုခြင်း)
* [(၅) NodeJS အခြေခံ](./index.md#၅-nodejs-အခြေခံ)
* [(၆) ClientJS Env နှင့် NodeJS Env](./index.md#၆-clientjs-env-နှင့်-nodejs-env)
* [(၇) Module များခွဲထုတ်ရေးသားခြင်း](./index.md#၇-module-များခွဲထုတ်ရေးသားခြင်း)

### 📒 အပိုင်း (၂)

* [(၈) ExpressJS ထည့်သွင်းခြင်း](./part-2.md#၈-expressjs-ထည့်သွင်းခြင်း)

[👆 မာတိကာသို့](#မာတိကာ)

---

## ~~~ 📒 အပိုင်း (၂) ~~~

### (၈) ExpressJS ထည့်သွင်းခြင်း

NodeJS ကိုအသုံးပြုပြီး web application တစ်ခုပြုလုပ်မည် ဆိုပါက http module ကိုအသုံးပြုပြီး web server ပြုလုပ်ကာ application အတွက်လိုသည်များကို အသေးစိတ်ပြုလုပ်နိုင်ပါသည်။ သို့သော်လည်း ထိုကဲ့သို့ အသေးစိတ် low level အထိလိုက်ရေးမနေဘဲ အသင့်ပြုလုပ်ထားသော framework များကို အသုံးပြုကား လွယ်ကူလျှင်မြန်စွာ application များကို တည်ဆောက်နိုင်မှာ ဖြစ်ပါသည်။ ထိုသို့ပြုလုပ်ရာတွင် web application များတွက် လူသုံးများပြီး၊ အလွန်အသုံးဝင်သော framework တစ်ခုမှာ ExpressJS ပင်ဖြစ်ပါသည်။ ExpressJS ကိုထည့်သွင်းရန် project directory ထဲတွင် အောက်ပါအတိုင်း terminal များရိုက်၍ install ပြုလုပ်ပါမည်။
```
npm i express
```
Install ပြုလုပ်ပြီးပါက `package.json` file ထဲရှိ dependencies အောက်တွင် install ပြုလုပ်ထားသော ExpressJS ၏ version အားတွေ့ရမည် ဖြစ်ပါသည်။ ထိုနောက် application အား စတင်ရေးသားရန် terminal ထဲတွင် `code .` ဟုရိုက်ကာ VSCode အားဖွင့်ပါမည်။ index file အားပြုလုပ်ရန် terminal ထဲတွင် `touch index.js` ဟုရိုက်ပါသည်။ ထိုနောက် အောက်ပါအတိုင်း index.js အား VSCode ထဲတွင် ရေးပါမည်။
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

[👆 မာတိကာသို့](#မာတိကာ)

---
