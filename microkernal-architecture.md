# 3 Microkernal Architecture

ဒီ patternကတော့Product-based applicationတွေတည်ဆောက်တဲ့အခါ အသုံးများတဲ့ patternတခု။ plug-in architecture patternလို့လည်းသိကြတယ်။ third-party productတခုအနေနဲ့ သူ့ချည်းသီးသန့် versions အလိုက် package အလိုက် download လုပ်ပြီး သုံးနိုင်တဲ့ applicationမျိုးကို  product-based applicationလို့ခေါ်လေ့ရှိကြတယ်။ ဒါပေမဲ့ တချို့ companyတွေကတော့ တခါတလေ internal business အတွက် software products တွေ့ pluggable features တွေအနေနဲ့ တည်ဆောက်တဲ့အခါမှာလည်း သုံးလေ့ရှိတယ်။ core applicationကို ထည့်ဖြည့်ပေးတဲ့ သီးခြား featuresတွေနဲ့ application ဆောက်မယ်ဆိုရင် သူက အသင့်တော်ဆုံးလို့ ပြောလို့ရတယ်။

### Pattern Description

ဒီarchitectureမှာ အဓိကအားဖြင့် core system နဲ့ plug-in modulesဆိုပြီးရှိမယ်။ application logicကို သီးသန့် plug-in modules တွေနဲ့ ၊ extensible လည်းဖြစ် flexibilityလည်းဖြစ်တဲ့ core systemဆိုပြီး ၂ ပိုင်းခွဲထားပါတယ်။&#x20;

core systemမှာ အခြေခံ functionလေးတွေပါ၀င်တတ်ပြီး၊ အသေးစိတ် အနုစိတ်processingတွေမပါ၀င်ဘဲ ယေဘူယဆန်ဆန် business logicတွေနဲ့ တည်ဆောက်ထားတယ်။ ပြီးတော့မှ independent component အနေနဲ့ plugin moduleတွေကို core systemနဲ့ချိတ်ဆက်ပြီး သုံးတဲ့ architectureပုံစံမျိုးပါ။ OS တွေဟာများသောအားဖြင့် microkernal architecuture pattern နဲ့တည်ဆောက်ထားတဲ့အတွက် ဒီpatternကို ခုလို နာမည်ပေးထားတာဖြစ်ပါတယ်။ ဒီတော့ plugin module တွေဟာ တနည်းနည်းနဲ့ core system ကို ချိတ်ဆက် communicate လုပ်ပြီး အလုပ်လုပ်ကြပါတယ်။ patternအနေနဲ့တော့ ဘယ်နည်းကိုသုံးပြီးမှ ချိတ်ဆက်ရမယ် လို့တော့ သီးခြားသတ်မှတ်မထားပါဘူး။ XML နဲ့ပဲချိတ်ချိတ် JSONနဲ့ပဲ dataတွေစီးဆင်းရင်ပဲဖြစ်ဖြစ် ၊ messaging သုံးသုံး ၊ လွတ်လပ်စွာ သုံးပြီးချိတ်ဆက် အလုပ်လုပ် လို့ရပါတယ်။&#x20;

<figure><img src=".gitbook/assets/image (6).png" alt=""><figcaption><p>Figure 3-1 Microkernal Architecture Pattern</p></figcaption></figure>

ဥပမာတခုအနေနဲ့ Eclipse IDE မှာ ဆိုရင် funcy editor featureလေးတွေ သုံးချင်မယ်ဆိုပါစို့။ ကိုယ်ကြိုက်နှစ်သက်တဲ့ editor plug-inတခု ထည့်ပြီး သုံးလိုက်ရုံပါပဲ။ customizable ဖြစ်ပီး အသုံး၀င်ပါတယ်။&#x20;

ဒါဆို ရှုပ်ထွေးကြီးမားတဲ့ business အတွက်ဆိုရင်ကော သူ့ကိုသုံးလို့မရနိုင်ဘူးလား ဆိုတော့ ရပါတယ်။ ဥပမာ insurance claims process တခုဆိုပါတော့၊ ကိုယ့်ကားရဲ့ windshield ကတခုခုနဲ့တိုက်မိပြီး ပျက်သွားတဲ့အတွက် လဲလှယ်ချင်တဲ့အတွက် claim လုပ်ချင်တယ်၊ တချို့ ပြည်နယ်တွေမှာက ခွင့်ပြုပေးပြီး တချို့မှာ ခွင့်မပြုဘူးဆိုကြပါစို့။ ဒီလိုမျိုး စတဲ့ အခြေနေတွေနဲ့ အမျိုးမျိုးသော conditionတွေဖြစ်လာနိုင်ပါတယ်။ အဲဒီ စည်းမျဥ်တခုခု ကိုပြောင်းလဲဖို့ဆိုရင် တခြားမှာလည်း အကျိုးသက်ရောက်စေနိုင်တဲ့အတွက် tester တွေ analystတွေ developerတွေက အမျိုးမျိုးစစ်ဆေးပြီး လုပ်ရမှာပါ။ ဒီလိုမျိုး အခြေအနေတွေမှာဆိုရင် ခွင့်ပြုထားတဲ့ ပြည်နယ်တွေမှာပဲ claim module ကို ထည့်ပေးရုံနဲ့ ဒီpatternက ပြဿနာကိုဖြေရှင်းနိုင်ပါတယ်။&#x20;



