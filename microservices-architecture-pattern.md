# 4 Microservices Architecture Pattern

Microservices ကတော့ ခုလက်ရှိအသုံးများနေတဲ့  monolithic applicationနဲ့ service-oriented architecure တွေအတွက် evolutionary pathတခုအနေနဲ့ တခြားရွေးချယ်စရာ architectureတခုပါ။ ခုထိလည်း တိုးတက်ပြောင်းလဲနေဆဲဖြစ်တာကြောင့် IT industryမှာလည်း implementလုပ်ပုံလုပ်နည်း ဒီpatternအကြောင်း အဓိပ္ပါယ်အမျိုးမျိုးနဲ့ ပုံဖော်နေကြတုန်းပါပဲ။&#x20;

အရင် patternတွေမှာ topology တွေ implementation styleတွေ ဘယ်လိုပဲ ရှိရှိ၊ သူတို့တွေထဲမှာ တူညီတဲ့ conceptသဘောတရားတွေ အများကြီးရှိပါတယ်။ အဲဒီထဲက တခုကတော့ သီးသန့် unit တခုအနေနဲ့ ခွဲထုတ်တဲ့ အယူအဆပါ။  microservices မှာ componenet တခုစီဟာ သီးခြား deployလုပ်နိုင်တဲ့အတွက် deploy လုပ်ရာမှာ လွယ်ကူတယ်၊ scalability ကောင်းတယ်။ decoupling ဖြစ်တယ်။ ပြင်ဆင်ရလွယ်ကူမယ်။ အဲဒီcomponentတွေဟာ single purpose functionတွေလည်းဖြစ်နိုင်တယ်  component တခုစီဟာ တခုထက်မကတဲ့ modules တွေ ပေါင်းထားတာလည်းဖြစ်နိုင်တယ်။ ကြီးမားတဲ့ ရှုပ်ထွေးတဲ့ applicationတွေတည်ဆောက်တဲ့အခါမှာ အဲလိုမျိုး service component တွေကို မှန်ကန်တဲ့ အထားအသိုနဲ့ တည်ဆောက်ဖို့ အရေးကြီးပါတယ်။

<figure><img src=".gitbook/assets/image (4).png" alt=""><figcaption><p>Figure 4-1 Basic Microservice architecture pattern</p></figcaption></figure>

နောက်ထပ် main conceptတခုကတော့ distributed ဖြစ်ခြင်းပဲဖြစ်တယ်။ componentတခုစီဟာ fully decoupled ဖြစ်ကြတယ်။ တခုနဲ့တခု access လုပ်ဖို့ဆိုရင် REST, JMS, AMQP, etc အစရှိတဲ့ remote access protocolတွေကိုသုံးပြီး ချိတ်ဆက်ကြပါတယ်။ ဒါဟာလည်း scalability နဲ့ deploymentအတွက် အထောက်အကူပြုစေပါတယ်။
