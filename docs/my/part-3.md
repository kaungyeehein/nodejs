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
* [(၁၀) Express Validator (To be continue)](./part-2.md)
* [(၁၁) Express Session (To be continue)](./part-2.md)
* [(၁၂) Express Messages (To be continue)](./part-2.md)
* [(၁၃) Connnect Flash (To be continue)](./part-2.md)

### 📒 အပိုင်း (၃)

* [(၀) Scheduler Jobs ထည့်သွင်းခြင်း](./part-3.md)

[👆 မာတိကာသို့](#မာတိကာ)

---

## ~~~ 📒 အပိုင်း (၃) ~~~

### (၀) Scheduler Jobs ထည့်သွင်းခြင်း

NodeJS ကိုအသုံးပြုပြီး Scheduled Batch Process များပြုလုပ်နိုင်ပါသည်။ သက်မှတ်ထားသော နေ့၊ ရက်၊ အချိန်တွင် တစ်ကြိမ်သာ ပြုလုပ်ရန် သို့မဟုတ် သက်မှတ်ထားသော အချိန်အတိုင်းအတာတွင် အကြိမ်ကြိမ်ပြုလုပ်ရန် စသည်ဖြင့် ပြုလုပ်နိုင်ပါသည်။ ထိုသို့ပြုလုပ်ရန် `node-schedule` package ကိုအောက်ပါအတိုင်း ထည့်သွင်းရန် လိုအပ်ပါသည်။
```
npm i node-schedule
```

#### Scheduled Job

ပြုလုပ်ချင်သော နေ့၊ ရက်၊ အချိန်အား သက်မှတ်ရန် `Date()` function အားအသုံးပြုကာ year, month, day, hour, minute, second အား ထည့်သွင်းပေးရမည် ဖြစ်ပါသည်။ သတိပြုရန်မှာ javascript တွင် month ကို zero(0) မှ eleven(11) အထိ January to December သက်မှတ် ထားပါသည်။ ထိုကြောင့် 2021 Sept 8 နေ့ ၁၀ နာရီတွင် ပြုလုပ်လိုပါက အောက်ပါအတိုင်း ရေးသားရမည် ဖြစ်ပါသည်။
```javascript
// app.js
const schedule = require('node-schedule');

//* At a particular Date & Time
//- in JavaScript - 0 - January, 11 - December
const someDate = new Date(2021, 8, 8, 10, 0, 0);

schedule.scheduleJob(someDate, () => {
    console.log('Job run @', new Date().toString());
});
```

#### Repetitive Job

အချိန်အတိုင်းအတာ တစ်ခုတွင် အကြိမ်ကြိမ် ပြန်လည်ပြုလုပ်လိုပါက Cron Expression ဖြင့်ရေးသားနိုင်ပါသည်။ Cron Expression ၏ အဓိက parameter ၅ ခုအား Star (\*) ၅ လုံးနဲ့ ဖေါ်ပြပြီး ၎င်းတို့မှာ Minute (0 - 59, Hour (0 - 23), Day of The Month (1 - 31), Month (1 - 12), Day of The Week (0-7, Sun, Sat) တို့ဖြစ်ပါသည်။ Cron Expression ရေးနည်းကို နမူနာ ကြည့်ရန် [crontab.guru](https://crontab.guru/) တွင် အသေးစိတ် လေ့လာနိုင်ပါသည်။
- `0 0 * * *` ဆိုပါက ည ၁၂ နာရီတိုင်းပြုလုပ်မည် ဖြစ်သည်၊
- `0 0 * * Sun` ဆိုပါက အပတ်စဉ် Sunday တိုင်း ည ၁၂ နာရီတွင်ပြုလုပ်မည် ဖြစ်သည်၊
- `0 0 * * Sat,Sun` ဆိုပါက အပတ်စဉ် Saturaday နှင့် Sunday တိုင်း ည ၁၂ နာရီတွင်ပြုလုပ်မည် ဖြစ်သည်၊
ဥပမာ 2 second တစ်ခါ အကြိမ်ကြိမ် ပြန်လည်ပြုလုပ်လိုပါက optional second parameter ကို အရှေ့ဆုံးတွင် အောက်ပါ Cron Expression အတိုင်း ထည့်သွင်း သက်မှတ်နိုင်ပါသည်။
```javascript
// app.js
const schedule = require('node-schedule');

//* At reocurrent intervals
schedule.scheduleJob('*/2 * * * * *', () => {
    console.log('I run..');
});
```

ထိုသို့ အကြိမ်ကြိမ် ပြုလုပ်နေသော အလုပ်ကို ရပ်နားချင်ပါက `cancelJob()` function ကိုခေါ်ယူ အသုံးပြုရမည် ဖြစ်ပါသည်။ ရပ်နားချင်သော အလုပ်ကို အောက်ပါအတိုင်း Job name သက်မှတ်ပေးထားရမည် ဖြစ်ပါသည်။
```javascript
// app.js
const schedule = require('node-schedule');

//* At reocurrent intervals
schedule.scheduleJob('m-job', '*/2 * * * * *', () => {
    console.log('I run..');
    schedule.cancelJob('m-job');
});
```
ထိုအခါ တစ်ကြိမ်သာ ပြုလုပ်၍ အလုပ်ကို ရပ်နားသွားမည် ဖြစ်ပါသည်။ Job name မသက်မှတ်လို့ပါက အောက်ပါအတိုင်း variable ထဲတွင် လက်ခံပြီး `cancel()` function ကိုခေါ်ယူ အသုံးပြုနိုင်ပါသည်။ ရလဒ်မှာ အတူတူပင်ဖြစ်ပါသည်။
```javascript
// app.js
const schedule = require('node-schedule');

//* At reocurrent intervals
const mJob = schedule.scheduleJob('*/2 * * * * *', () => {
    console.log('I run..');
    mJob.cancel();
});
```
`node-schedule` package ၏အားသာချက်မှာ Cron Expression ဖြင့်ရေးသားနိုင်သလို Cron Expression မဟုတ်သော နည်းလမ်းဖြင့်လည်း ရေးသားနိုင်ပါသည်။ အသေးစိတ်လေ့လာလိုပါက [node-schedule](https://www.npmjs.com/package/node-schedule) တွင်လေ့လာနိုင်ပါသည်။ `node-schedule` ကဲ့သို့ Scheduled Batch Process များ ပြုလုပ်နိုင်သော အခြား package များလည်းရှိပါသည်။ ၎င်းတို့မှာ [agenda](https://www.npmjs.com/package/agenda) နှင့် [node-cron](https://www.npmjs.com/package/node-cron) တို့ပဲဖြစ်ပါသည်။

---
