# ကိုကောင်း၏ NodeJS မှတ်စု

## မာတိကာ

1. [NodeJS မိတ်ဆက်](#၁-nodejs-မိတ်ဆက်)
2. [NodeJS ကိုထည့်သွင်းခြင်း](#၂-NodeJS-ကိုထည့်သွင်းခြင်း)
3. [Project Directory ပြုလုပ်ခြင်း](#၃-Project-Directory-ပြုလုပ်ခြင်း)

[👆 မာတိကာသို့](#မာတိကာ)

---

### (၁) NodeJS မိတ်ဆက်

NodeJS ဆိုသည်မှာ V8 JavaScript Engine ကို အသုံးပြုထားပြီး JavaScript ကို server side တွင် အသုံးပြုလို့ရအောင် ပြုလုပ်ပေးသော runtime environment တစ်ခုဖြစ်သည်။ NodeJS သည် open-source ဖြစ်ပြီး၊ မည်သည့် operating system တွင်မဆို အသုံးပြုနိုင်သော cross-platform အမျိုးအစားလဲ ဖြစ်ပါသည်။ NodeJS ကိုလေ့လာမည်ဆိုပါက JavaScript ကို သိရှိနားလည်ထားဖို့ လိုအပ်ပြီး၊ အဓိကအားဖြင့် JavaScript ၏ အောက်ပါအကြောင်းအရာများကို ကြိုတင်လေ့လာထားသင့် ပါသည်။

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
NodeApp directory ကိုပြုလုပ်ပြီး၊ `package.json`file ကိုပါပြုလုပ်သွားမည် ဖြစ်သည်။


[👆 မာတိကာသို့](#မာတိကာ)

---