# ကိုကောင်း၏ NodeJS မှတ်စု

Language: MY|[EN](../en/)

## မာတိကာ

1. [NodeJS မိတ်ဆက်](#၁-nodejs-မိတ်ဆက်)
2. [NodeJS ကိုထည့်သွင်းခြင်း](#၂-nodejs-ကိုထည့်သွင်းခြင်း)
3. [Project Directory ပြုလုပ်ခြင်း](#၃-project-directory-ပြုလုပ်ခြင်း)
4. [VSCode အသုံးပြုခြင်း](#၄-vscode-အသုံးပြုခြင်း)
5. [NodeJS အခြေခံ](#၅-nodejs-အခြေခံ)

[👆 မာတိကာသို့](#မာတိကာ)

---

### (၁) NodeJS မိတ်ဆက်

NodeJS ဆိုသည်မှာ V8 JavaScript Engine ကို အသုံးပြုထားပြီး JavaScript ကို server side တွင် အသုံးပြုလို့ရအောင် ပြုလုပ်ပေးသော runtime environment တစ်ခုဖြစ်သည်။ V8 ဆိုသည်မှာ Google Chrome Browser တွင် အသုံးပြုထားသော JavaScript Engine ဖြစ်ပါသည်။ NodeJS သည် open-source ဖြစ်ပြီး၊ မည်သည့် operating system တွင်မဆို အသုံးပြုနိုင်သော cross-platform အမျိုးအစားလဲ ဖြစ်ပါသည်။ NodeJS ကိုလေ့လာမည်ဆိုပါက JavaScript ကို သိရှိနားလည်ထားဖို့ လိုအပ်ပြီး၊ အဓိကအားဖြင့် JavaScript ၏ အောက်ပါအကြောင်းအရာများကို ကြိုတင်လေ့လာထားသင့် ပါသည်။

* Lexical Structure
* Expressions
* Types
* Classes
* Variables
* Functions
* this
* Arrow Functions
* Loops
* Scopes
* Arrays
* Template Literals
* Semicolons
* Strict Mode
* ECMAScript 6, 2016, 2017

NodeJS သည် asynchronous programming ဖြစ်ပါသည်။ asynchronous ဆိုသည်မှာ program ၏ instruction များကို တစ်ခုပြီးမှတစ်ခု အစဉ်လိုက် ပြီးအောင် စောင့်စရာမလိုပဲ ဆက်လက် ပြုလုပ်သွားနိုင်ခြင်းဖြစ်သည်။ အဓိကအနေဖြင့် NodeJS ၏ အခြေခံမှာ အောက်ပါတို့ ပါဝင်သည်။

* Asynchronous programming and callbacks
* Timers
* Promises
* Async and Await
* Closures
* The Event Loop

[👆 မာတိကာသို့](#မာတိကာ)

---

### (၂) NodeJS ကိုထည့်သွင်းခြင်း

NodeJS ကိုထည့်သွင်းရန် [https://nodejs.org](https://nodejs.org) သို့သွားရောက်၍ download လုပ်ပြီး၊ install ပြုလုပ်ပါ။ NodeJS ကို install ပြုလုပ်ပါက `node` နှင့် `npm` ကို အလိုအလျောက် ထည့်သွင်းသွားမည် ဖြစ်သည်။ `node` သည် NodeJS run ပေးသော command ဖြစ်ပြီး၊ `npm` သည် NodeJS နှင့် ဆက်စပ်နေသော package များကို install လုပ်ပေးသော command ဖြစ်သည်။

Install ပြုလုပ်ထားသော `node` နှင့် `npm` ၏ version များကို အောက်ပါအတိုင်း စစ်ဆေးနိုင်ပါသည်။
```
npm -v
node -v
```

NodeJS ကို နောက်ဆုံး version သို့ မြှင့်တင်ချင်ပါက အောက်ပါအတိုင်း ပြုလုပ်နိုင်ပါသည်။
```
sudo npm i -g npm
sudo npm i -g n
```

[👆 မာတိကာသို့](#မာတိကာ)

---

### (၃) Project Directory ပြုလုပ်ခြင်း

Project directory ပြုလုပ်ရန် `mkdir`, `cd` နှင့် `npm` command များကို အသုံးပြုသွားမည် ဖြစ်သည်။
```
mkdir NodeApp
cd NodeApp
npm init -y
```
NodeApp directory ကိုပြုလုပ်ပြီး၊ `package.json`file ကို default option များနှင့် ပြုလုပ်သွားမည် ဖြစ်သည်။ `package.json` သည် NodeJS Project အတွက် version သက်မှတ်ခြင်းနှင့် လိုအပ်သော package များထည့်သွင်းရန် အရေးပါသော file ဖြစ်သည်။

Application တစ်ခု တည်ဆောက်ရန် `app.js` အမည်ဖြင့် file တစ်ခုအားပြုလုပ်၍ အောက်ပါအတိုင်း ရေးကြည့်ပါမည်။
```javascript
// app.js
console.log('Hello World!');
```
File ရေးပြီးသွားပါက `node` command ကိုအသုံးပြုပြီး အောက်ပါအတိုင်း run ကြည့်ပါက 'Hello World!' ဆိုသော စာသားကို output အနေဖြင့် မြင်ရမည်ဖြစ်ပါသည်။
```
node app.js
```

[👆 မာတိကာသို့](#မာတိကာ)

---

### (၄) VScode အသုံးပြုခြင်း

Application များကို nodepad သို့မဟုတ် နှစ်သက်ရာ IDE အသုံးပြု၍ ရေးသားနိုင်ပါသည်။ သို့သော် Microsoft ကပြုလုပ်ထားသော Visual Studio Code Editor (VScode) ကို အသုံးပြုရန် အကြံပေးပါသည်။ JavaScript development အတွက် လိုအပ်သော၊ ကောင်းမွန်သော extensions ပေါင်းများစွာ VScode တွင်ရှိသောကြောင့် ဖြစ်ပါသည်။ Sublime Text ကဲ့သို့သော editing feature များ၊ file auto saving feature များ စသည်ဖြင့် အသုံးဝင်သော feature ပေါင်းများစွာလဲ ရှိပါသည်။

VScode ကိုထည့်သွင်းရန် [https://code.visualstudio.com](https://code.visualstudio.com) သို့သွားရောက်၍ download လုပ်ပြီး၊ install ပြုလုပ်ပါ။ Install ပြုလုပ်ပြီးပါက အောက်ပါ extensions များကိုလည်း ထည့်သွင်းပါ။

* Material Icon Theme (Project directory ထဲတွင် file များ၊ directory များကို လွယ်ကူစွာ မြင်နိုင်ရန်)
* Bracket Pair Colorizer 2 (Program ထဲတွင် အဖွင့်/အပိတ် ကွင်းများကို လွယ်ကူစွာ မြင်နိုင်ရန်)
* Import Cost (JavaScript တွင် import/require လုပ်ထားသော package များ၏ size ကိုသိရန်)
* MarkdownLint (Markdown file များကိုရေးရာတွင် code highlight လုပ်ရန်)
* DotENV (DotENV file ကိုရေးရာတွင် code highlight လုပ်ရန်)
* REST Client (REST API ရေးရာတွင် code များကို VScode ထဲတွင် စစ်ဆေးနိုင်ရန်)
* ESLint (Code syntax များ စစ်ဆေးရန်)

စသည်ဖြင့် အသုံးဝင်သော extensions ပေါင်းများစွာရှိပါသည်။ အခြားလိုအပ်သော extensions များလည်း ရှာဖွေထည့်သွင်း အသုံးပြုနိုင်ပါသည်။

[👆 မာတိကာသို့](#မာတိကာ)

---

### (၄) NodeJS အခြေခံ

NodeJS တွင် အရေးပါသော လုပ်ဆောင်ချက်မှာ Non-blocking I/O ဖြစ်ပါတယ်။ JavaScript သည် single threaded ပေါ်တွင် parallel processing ပြုလုပ်နိုင်သော language ဖြစ်သည်။ ပထမ အလုပ် ပြီးမြောက်အောင် စောင့်စရာမလိုပဲ မပြီးခင်မှာ ဒုတိယ အလုပ်ကို ဆက်လက် လုပ်ဆောင်နိုင်ခြင်းဖြစ်သည်။ ဥပမာ Network ပေါ်က အကြောင်းအရာ တစ်ခုခုကို တောင်းဆိုနေချိန်တွင် အခြားအလုပ်များကို ဆက်လက်လုပ်ဆောင် နိုင်ခြင်းဖြစ်သည်။ ထိုသို့ပုံစံများကို JavaScript တွင် callback function များဖြင့် ရေးသားနိုင်ပါသည်။ အောက်ပါ နာမူနာ code ကို ကြည့်ပါ။
```JavaScript
console.log('Before');
window.addEventListener('load', () => {
  //window loaded
  console.log('Window loaded');
});
console.log('After');
```
ထို JavaScript code ကို browser တွင် run ကြည့်ပါက အောက်ပါအတိုင်း output ကိုရမည် ဖြစ်သည်။
```
Before
After
Window loaded
```
After ကို output ထုတ်ပြဖို့အတွက် window ကို loading ပြီးသည်အထိ စောင့်စရာမလိုပဲ ဆက်လက်လုပ်ဆောင်နိုင်ရန် callback အား arrow function အသုံးပြု၍ ရေးသားထားခြင်း ဖြစ်ပါသည်။ Window loading ပြီးမြောက်ပါက callback function က အလုပ်လုပ်မည် ဖြစ်ပါသည်။

[👆 မာတိကာသို့](#မာတိကာ)

---