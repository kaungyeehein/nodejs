# Git Command

`git init` Git Repository ကို local တွင် တည်ဆောက်ရန် အသုံးပြုပါသည်။

`git add <file_name>` ပြုလုပ်ထားသော file များအား Git Repository ၏ stage control တွင်ထည့်ရန် အသုံးပြုပါသည်။ လက်ရှိ directory အောက်က file များအားလုံး ထည့်ရန် `git add .` command အားအသုံးပြုနိုင်ပါသည်။

`git clone <Git_URL>` GitHub ကရှိပြီးသား Repository ကို ဆက်လက် အသုံးပြုလိုပါက အသုံးပြုရပါသည်။

`git commit -m "<message>"` အပြောင်းအလဲ ပြုလုပ်ထားသည်များကို local repository တွင် သိမ်းဆည်းရန် အသုံးပြုရပါသည်။

`git commit -a -m "<message>"` git add နှင့် git commit ကို ပေါင်းစပ်အသုံးပြုခြင်း ဖြစ်ပါသည်။

`git log` Git Repository တွင် commit ပြုလုပ်ထားသော history များကို ပြန်လည် ကြည့်ရှုရန် အသုံးပြုပါသည်။

`git remote -v` ဖြင့်ကြည့်ရှုပါက မည်သည့် GitHub Repository ကနေ remote ချိတ်ဆက်ထားသည်ကို မြင်နိုင်ပြီး၊ `git clone` command အသုံးပြုထားပါက auto ချိတ်ဆက်နေမည် ဖြစ်ပါသည်။

`git remote add <remote_name> <remote_url>` Git Repository အား `git init` ဖြင့်တည်ဆောက်ထားပါက GitHub Repository ကိုချိတ်ဆက်ရန် အသုံးပြုပါသည်။

`git remote remove <remote_name>` Git Repository ထဲတွင် GitHub Repository ၏ ချိတ်ဆက်ထားမှုများကို ဖျက်ပစ်ရန် အသုံးပြုပါသည်။

`git pull` GitHub Repository ကနေ update များကို ယူရာတွင် အသုံးပြုပါသည်။

`git push` GitHub Repository ကို update များ ပြန်လည် ပေးပို့ရာတွင် အသုံးပြုပါသည်။

`git branch` Local Repository ထဲရှိ branch list ကို မြင်ရမှာ ဖြစ်ပါသည်။ `git branch -r` ကိုအသုံးပြုပါက GitHub Repository ထဲရှိ branch list ကို မြင်ရမှာ ဖြစ်ပြီး၊ `git branch -a` ကိုအသုံးပြုပါက အားလုံးကို မြင်ရမှာ ဖြစ်ပါသည်။

`git checkout <branch_name>` လက်ရှိ အလုပ်လုပ်မည် branch အားရွေး ချယ်ရာတွင် အသုံးပြုပါသည်။

`git branch <branch_name>` Local Repository ထဲတွင် branch အသစ်တည်ဆောက်ရာတွင် အသုံးပြုပါသည်။

`git branch -m <new_name>` Local Repository ထဲတွင် လက်ရှိ branch အား အမည်ပြောင်းရာတွင် အသုံးပြုပါသည်။

`git branch -d <branch_name>` Local Repository ထဲရှိ branch အား ဖျက်ရာတွင်အသုံးပြုပါသည်။

`git push origin --delete <branch_name>` GitHub Repository မှာရှိသော branch ကို ဖျက်ပစ်ရန် အသုံးပြုပါသည်။

`git fetch <remote_name>` GitHub Repository ကနေ အားလုံးကို update လုပ်ရန် အသုံးပြုပါသည်။

`git config --list` Local Repository ထဲတွင် သက်မှတ်ထားသော configuration များကို တွေ့မြင်နိုင်ပါသည်။