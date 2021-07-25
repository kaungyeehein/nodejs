# ကိုကောင်း၏ NodeJS မှတ်စု

Language: MY|[EN](../en/index.md)

## မာတိကာ

1. [NodeJS မိတ်ဆက်](#၁-nodejs-မိတ်ဆက်)
2. [NodeJS ကိုထည့်သွင်းခြင်း](#၂-nodejs-ကိုထည့်သွင်းခြင်း)
3. [Project Directory ပြုလုပ်ခြင်း](#၃-project-directory-ပြုလုပ်ခြင်း)
4. [VSCode အသုံးပြုခြင်း](#၄-vscode-အသုံးပြုခြင်း)
5. [NodeJS အခြေခံ](#၅-nodejs-အခြေခံ)
6. [Import Export Module](#၆-import-export-module)

[👆 မာတိကာသို့](#မာတိကာ)

---

### (၁) NodeJS မိတ်ဆက်

NodeJS ဆိုသည်မှာ V8 JavaScript Engine ကို အသုံးပြုထားပြီး JavaScript ကို server side တွင် အသုံးပြုလို့ရအောင် ပြုလုပ်ပေးသော runtime environment တစ်ခုဖြစ်သည်။ V8 ဆိုသည်မှာ Google Chrome Browser တွင် အသုံးပြုထားသော JavaScript Engine ပင်ဖြစ်သည်။ NodeJS သည် open-source ဖြစ်ပြီး၊ မည်သည့် operating system တွင်မဆို အသုံးပြုနိုင်သော cross-platform အမျိုးအစားလဲ ဖြစ်ပါသည်။ NodeJS ကိုလေ့လာမည်ဆိုပါက JavaScript ကို သိရှိနားလည်ထားဖို့ လိုအပ်ပြီး၊ အဓိကအားဖြင့် JavaScript ၏ အောက်ပါအကြောင်းအရာများကို ကြိုတင်လေ့လာထားသင့် ပါသည်။

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

### (၅) NodeJS အခြေခံ

NodeJS တွင် အရေးပါသော လုပ်ဆောင်ချက်မှာ Non-blocking I/O ဖြစ်ပါတယ်။ JavaScript သည် single threaded ပေါ်တွင် parallel processing ပြုလုပ်နိုင်သော language ဖြစ်သည်။ ပထမ အလုပ် ပြီးမြောက်အောင် စောင့်စရာမလိုပဲ မပြီးခင်မှာ ဒုတိယ အလုပ်ကို ဆက်လက် လုပ်ဆောင်နိုင်ခြင်းဖြစ်သည်။ ဥပမာ Network ပေါ်က အကြောင်းအရာ တစ်ခုခုကို တောင်းဆိုနေချိန်တွင် အခြားအလုပ်များကို ဆက်လက်လုပ်ဆောင် နိုင်ခြင်းဖြစ်သည်။ ထိုသို့ပုံစံများကို JavaScript တွင် callback function များဖြင့် ရေးသားနိုင်ပါသည်။ အောက်ပါ နာမူနာ code ကို ကြည့်ပါ။

#### Callback

```javascript
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
After ကို output ထုတ်ပြဖို့အတွက် window ကို loading ပြီးသည်အထိ စောင့်စရာမလိုပဲ ဆက်လက်လုပ်ဆောင်နိုင်ရန် callback အား arrow function အသုံးပြု၍ ရေးသားထားခြင်း ဖြစ်ပါသည်။ Window loading ပြီးမြောက်ပါက callback function က အလုပ်လုပ်မည် ဖြစ်ပါသည်။ နောက်ထပ် ဥပမာ တစ်ခုထပ်ကြည့်ရအောင်။

#### Timer

```javascript
const funA = () => console.log('Function A');
const funB = () => console.log('Function B');
const funC = () => {
  console.log('Function C');
  setTimeout(funA, 0);
  funB();
};

funC();
```
ထို JavaScript code ကို browser တွင် run ကြည့်ပါက အောက်ပါအတိုင်း output ကိုရမည် ဖြစ်သည်။
```
Function C
Function B
Function A
```
Timer function တွင် funA ကို ချက်ချင်းအလုပ်လုပ်ရန် 0 (zero) timer ထားပြီး ခေါ်သော်လည်း၊ funB အလုပ်ပြီးမှ funA ကို ခေါ်သည်ကို တွေ့မြင်ရပါသည်။ အဘယ့်ကြောင့်ဆိုသော် Timer function သည် JavaScript ၏ call stack ထဲတွင် လုပ်စရာမရှိတော့မှ နောက်ဆုံး လုပ်ပေးသောကြောင့် ဖြစ်သည်။

JavaScript သည် default အားဖြင့် asynchronous ပုံစံဖြစ်ပြီး၊ synchronous ပုံစံ ရေးသားလိုပါက callback function ထဲတွင် ထည့်သွင်းရေးသား နိုင်ပါသည်။ သို့သော် Callback function ထဲတွင်လည်း callback function များ ထပ်ခါထပ်ခါ ရေးသားပါက နားလည်ရ ခက်ခဲလာနိုင်ပါသည်။ ထိုပြဿနာကို ပြေလည်နိုင်ရန် ES6 တွင် Promises ရေးထုံးကို ထည့်သွင်းလာခဲ့ပါသည်။

#### Promises

Promises သည် timer ကဲ့သို့ call stack အဆုံးထိ စောင့်စရာမလိုပဲ တက်နိုင်သလောက် မြန်မြန် ပြုလုပ်ပေးနိုင်သော ရေးနည်းဖြစ်သည်။ ထို့အပြင် promises များကို တစ်ခုနှင့် တစ်ခု ချိတ်ဆက်ပြီး chain လိုမျိုး ရေးသားနိုင်သေးသည်။
```javascript
const funA = () => console.log('Function A');
const funB = () => console.log('Function B');
const funC = () => {
  console.log('Function C');
  setTimeout(funA, 0);

  const p = new Promise((resolve, reject) => {
    resolve('After funB, Before funA');
  });
  p.then(result => console.log(result))
    .catch(error => console.error(error));

funB();
};

funC();
```
ထို JavaScript code ကို browser တွင် run ကြည့်ပါက အောက်ပါအတိုင်း output ကိုရမည် ဖြစ်သည်။
```
Function C
Function B
After funB, Before funA
Function A
```
Promise function p() သည် Timer အသုံးပြုထားသော funA ကဲ့သို့ call stack ဆုံးသည့်အထိ စောင့်စရာ မလိုပဲ အရင်ပြုလုပ်သွားသည်ကို တွေ့မြင်နိုင်မည် ဖြစ်ပါသည်။ Promise function တွင် resolve နှင့် reject ဟူသော parameter နှစ်ခုကို ထည့်ပေးရမည် ဖြစ်သည်။ function ထဲတွင် လုပ်ဆောင်ချက် အောင်မြင်ပါက resolve ကို ခေါ်ရမည်ဖြစ်ပြီး၊ မအောင်မြင်ပါက reject ကိုခေါ်ရမည် ဖြစ်သည်။ ထို promise ကို ပြန်လည်အသုံးပြုလိုပါက then နဲ့ catch ကို အသုံးပြုရမည် ဖြစ်သည်။ then ဖြင့် promise များတစ်ခုမက ချိတ်ဆက် အသုံးပြုနိုင်ပါသည်။ Promise ကိုအသုံးပြုပါက `new` keywoard ဖြင့် `new Promise()` ဟုသာအသုံးပြုလို့ရကြောင်း မှတ်သားစေချင်ပါသည်။

#### Async and Await

ES2017 တွင် Promise ကို ပိုမိုလွယ်ကူအောင် async/await ရေးထုံးနှင့် ရေးသားနိုင်ပါသည်။ ၎င်း၏ နောက်ကွယ်တွင် promise ကိုပင် အသုံးပြုထားခြင်း ဖြစ်သည်။ နာမူနာ code ကို ကြည့်လိုက်ကြရအောင်။
```javascript
const doSomethingAsync = () => {
  return new Promise(resolve => {
    setTimeout(() => resolve('Do something after 3sec'), 3000);
  });
};

const doSomething = async () => {
  console.log(await doSomethingAsync());
}

console.log('Before');
doSomething();
console.log('After');
```
ထို JavaScript code ကို browser တွင် run ကြည့်ပါက အောက်ပါအတိုင်း output ကိုရမည် ဖြစ်သည်။
```
Before
After
Do something after 3sec
```
`async` လို function အား သက်မှတ်လိုက်ချင်းသည် ၎င်း function သည် promise ကို return ပြန်နိုင်သည်ဟု ဖေါ်ပြခြင်းဖြစ်သည်။ `await` keyword ဖြင့် async function များကို ခေါ်ရာတွင်လဲ ၎င်း function မှာ resolve သို့မဟုတ် reject ကို return ပြန်မရမခြင်း ရပ်နေမည်ဖြစ်သည်။

အောက်ပါ ဥပမာတွင် Promise change ကိုအသုံးပြု၍ json data ကိုရယူထားခြင်းဖြစ်သည်။
```javascript
const getFirstUserData = () => {
  return fetch('/users.json') // get users list
    .then(response => response.json()) // parse JSON
    .then(users => users[0]) // pick first user
    .then(user => fetch(`/users/${user.name}`)) // get user data
    .then(userResponse => userResponse.json()) // parse JSON
};

getFirstUserData();
```
Promise change များကိုလည်း ပိုမိုရှင်းလင်းသော ပုံစံဖြစ်စေရန် အောက်ပါ async/await ပုံစံအတိုင်း ပြောင်းလဲ ရေးသားနိုင်ပါသည်။
```javascript
const getFirstUserData = async () => {
  const response = await fetch('/users.json'); // get users list
  const users = await response.json(); // parse JSON
  const user = users[0]; // pick first user
  const userResponse = await fetch(`/users/${user.name}`); // get user data
  const userData = await userResponse.json(); // parse JSON
  return userData;
};

getFirstUserData();
```
Asynchronous function များသည် debug လိုက်ဖို့ခက်ခဲပေမဲ့လည်း ထိုသို့ async/await ပုံစံ ပြောင်းရေးပါက synchronous function လို debug လိုက်ဖို့ လွယ်ကူလာတာကို တွေ့ရမည် ဖြစ်ပါသည်။

နောက် ဥပမာ တစ်ခုတွင် file တစ်ခုအား ဖွင့်ပုံကို synchronous ပုံစံ ရေးပြပါမည်။
```javascript
const fs = require('fs');

try {
  const fd = fs.openSync('/Users/joe/test.txt', 'r');
  // Other task wait to run after this function finish
} catch (err) {
  console.error(err);
}
```
ထို code ပုံစံအတိုင်း file တစ်ခုအား ဖွင့်ပုံကို asynchronous ပုံစံ ရေးပြပါမည်။
```javascript
const fs = require('fs');

fs.open('/Users/joe/test.txt', 'r', (err, fd) => {
  // Other task don't wait to run after this function finish
});
```

ယခုရှင်းပြသော NodeJS အခြေခံများကို အသေးစိတ် သိရှိလိုပါက အောက်ဖေါ်ပြပါ website တွင် ဆက်လက်လေ့လာပါရန် တိုက်တွန်းပါသည်။

* [https://nodejs.dev/learn](https://nodejs.dev/learn)
* [https://nodeschool.io/](https://nodeschool.io/)

[👆 မာတိကာသို့](#မာတိကာ)

---

### (၆) Import Export Module

Function များကို ရှင်းလင်းစွာ မြင်နိုင်ရန်နှင့် ထပ်ခါထပ်ခါ အသုံးပြုနိုင်ရန် module များခွဲထုတ်၍ export လုပ်ထားပြီး၊ အခြားတစ်ခုမှ import လုပ်ကာ ပြန်လည်အသုံးပြုနိုင်ပါသည်။ အမှတ်မှားတက်သည်မှာ client side JavaScript တွင် ရေးသော ES6 import export ရေးထုံးနှင့် NodeJS တွင် ရေးသော CommonJS import export ရေးထုံး ကိုမှားယွင်း မှတ်သားတက်ကြပါသည်။ ပထမဦးစွာ client side Javascript တွင် သုံးသော ES6 import export ကိုလေ့လာကြည့်ရအောင်။

#### ES6 Import Export (Client Side JS)

Variable name, function name, class name များ၏ ရှေ့တွင် `export` keyword ကိုရေး၍ export ပြုလုပ်နိုင်ပါသည်။ Module တစ်ခုတွင် `export` များစွာ ကြေငြာနိုင်သော်လဲ၊ `default` တစ်ခုသာ ကြေငြာနိုင်ပါသည်။
```javascript
// greeting.js
export default function hello() {
  console.log('Hello');
}
export function world() {
  console.log('World!');
}
```
ထိုကဲ့သို့ မရေးပဲ အောက်တွင် သီးသန့် export {} ရေး၍လည်း ပြုလုပ်နိုင်ပါသေးသည်။
```javascript
// greeting.js
function hello() {
  console.log('Hello');
}
function world() {
  console.log('World!');
}

export { hello as default, world };
```
ထိုကဲ့သို့ export လုပ်ထားသော `greeting.js` module ကို import ပြုလုပ်၍ ပြန်လည် အသုံးပြုပြပါမည်။ Default export ကို ဒီအတိုင်း ရှေ့ဆုံးတွင် import လုပ်နိုင်သော်လဲ၊ ရိုးရိုး named export သီးသန့်ကိုတော့ တွန့်ကွင်း {} ထဲတွင်ထည့်၍ import လုပ်ယူရမည် ဖြစ်သည်။
```javascript
import hello, { world } from "./greeting.js";

hello();
world();
```

#### CommonJS Import Export (NodeJS)

NodeJS မှာတော့ CommonJS Import Export ရေးထုံးသာ အသုံးပြုလို့ရမယ်လို့ မှတ်သားထားရမှာ ဖြစ်ပါတယ်။ ES6 မှာလို့ `export` မဟုတ်ဘဲ `exports` မှာ (s) ပါတာကို သတိထားရမှာ ဖြစ်ပါတယ်။ ၎င်း `exports` သည် module object မှလာတာဖြစ်ပြီး၊ default export လည်းမရှိသည်ကို သတိပြုရမည် ဖြစ်ပါသည်။
```javascript
// greeting.js
exports.hello = function() {
  console.log('Hello');
};
exports.world = function() {
  console.log('World!');
}
```
ထိုကဲ့သို့ မရေးပဲ အောက်တွင် သီးသန့် module.exports = {} ရေး၍လည်း ပြုလုပ်နိုင်ပါသေးသည်။
```javascript
// greeting.js
function hello() {
  console.log('Hello');
}
function world() {
  console.log('World!');
}

module.exports = { hello, world }; 
```
ထိုကဲ့သို့ export လုပ်ထားသော `greeting.js` module ကို import ပြုလုပ်၍ ပြန်လည် အသုံးပြုပြပါမည်။ ES6 မှာလို import key ကို အသုံးမပြုပဲ require() function ကိုသာ အသုံးပြုနိုင်ကြောင်း မှတ်သားထားရပါမည်။ Import သွင်းလိုသော module ကို variable တစ်ခုနှင့် assign လုပ်ထားရမည်ဖြစ်ပြီး၊ အသုံးပြုလိုပါက variable.function() ပုံစံဖြင့် ခေါ်ယူအသုံးပြုရမှာဖြစ်ပါသည်။
```javascript
const greeting = require('./greeting.js');

greeting.hello();
greeting.world();
```
ထိုကဲ့သို မခေါ်ချင်ဘဲ တိုက်ရိုက် အသုံးပြုလိုပါက object destructuring ပြုလုပ်၍ အသုံးပြုရမည် ဖြစ်ပါသည်။ အသုံးပြုပုံမှာ တွန့်ကွင်း {} ကိုအသုံးပြု၍ module ထဲမှာ import လုပ်ချင်သော function ကို တိုက်ရိုက် ခေါ်သုံးခြင်း ဖြစ်ပါသည်။
```javascript
const {hello, world} = require('./greeting.js');

hello();
world();
```

[👆 မာတိကာသို့](#မာတိကာ)

---