# 2 Event-Driven Architecture

Event-Driven architecture pattern ကတော့ highly scalable applications တွေအတွက် popular ဖြစ်တဲ့ pattern တခုပါ။ သူက distributed asynchronous architecture pattern အဖြစ်လည်း အသိများတယ်။ applicationက သေးသေးလား ကြီးကြီးလား၊ ရှုပ်ထွေးလား ရိုးရှင်းလား၊ ဘာနဲ့မဆို အဆင်ပြေတဲ့ highly adaptable ဖြစ်တဲ့ pattern တခုပါ။  decoupled ဖြစ်ပြီး၊ process တွေကို async နဲ့ အလုပ်လုပ်နိုင်တဲ့ single purpose event တွေအဖြစ်  components ကို ဖွဲ့စည်းထားတာဖြစ်တယ်။&#x20;

ဒီ pattern architecture မှာ Mediator နဲ့ Brokerဆိုပြီး အဓိက topologies ၂ ခုရှိပါတယ်။ Mediator topology ဆိုတာက ဗဟို mediator ကနေပြီး event တခုထဲမှာပဲ သူ့ရဲ့ အဆင့်ဆင့်လုပ်ဆောင်တာတွေကို စီမံခန့်ခွဲပေးရမယ် စုစည်းပေးရမဲ့အခြေနေမျိုးမှာသုံးလေ့ရှိတယ်။ Broker topology ကကျတော့ ကြားခံ mediatorမသုံးဘဲနဲ့ events တွေကြားမှာ ချိတ်ဆက်ဖို့အတွက်သုံးလေ့ရှိတယ်။ ကိုယ့်ရဲ့ applicationမှာအခြေနေအရ ဘယ်တခုနဲ့ ကိုက်ညီလဲ ဆိုတာကို ဆုံးဖြတ်ဖို့တော့ လိုအပ်တာပေါ့။&#x20;

Mediator Topology&#x20;

အပေါ်က ရှင်းလင်းချက်ကိုပဲ ဥပမာ တခုနဲ့ပြမယ်ဆိုရင် ပိုပြီး ရှင်းလင်းမြင်သာမယ် ထင်ပါတယ်။ stock ရှယ်ယာအရောင်း၀ယ် အတွက် eventတခုဆိုကြပါတော့။ အရင်ဆုံး stockကို သက်မှတ်ထားတဲ့ အချက်လက်တွေနဲ့ ကိုက်ညီမှုရှိမရှိ စီစစ်ပြီး အတည်ပြုမယ်။ brokerတွေဆီကို assignချပြီး commission တွက်မယ်။ နောက်ဆုံး tradeလုပ်ပြီးတဲ့အထိ။ ဒီလိုအဆင့်ဆင့်တွေ အကုန်လုံးမှာ ဘယ်အဆင့်ကတော့ပြီးရင် နောက်ဘယ်အဆင့်ဆက်သွားရမယ်၊ တပြိုင်နက်ထဲ ဘယ်အဆင့်တွေကတော့ လုပ်လို့ရတယ် ဆိုတာကို levelအလိုက်သတ်မှတ်ဖို့လိုအပ်လာတယ်ဆိုပါစို့။&#x20;

ဒီ architecture မှာ အဓိက ပါ၀င်တဲ့ component အနေနဲ့ Event queues, mediator, channels, နဲ့ processors ဆိုပြီး၄ ခုရှိတယ်။ အရင်ဆုံး clientကနေပြီး ပို့လိုက်တဲ့ eventတခုက queueထဲကိုရောက်မယ်။ mediator က သူ့ကို သက်ဆိုင်တဲ့ channel တွေဆီကို စီစစ်ပြီး ပို့ပေးမယ်။ processor ကတော့ တကယ်တမ်း သူနဲ့သက်ဆိုင်တဲ့ businuess logicတွေကို လုပ်ဆောင်မယ့် သူပေ့ါ။&#x20;

<figure><img src=".gitbook/assets/image.png" alt=""><figcaption><p>Figure 2-1. Event-driven Architecture Mediator Topology</p></figcaption></figure>

Broker Topology

သူနဲ့ mediatorနဲ့ကွာခြားချက်က တခုထဲက အလယ်ကနေ ကြားခံဖြန့်ကျက်ပေးတာမဟုတ်ဘဲနဲ့ event message တွေကို processor တွေဆီ ဖြန့်ပေးတဲ့ပုံစံမျိုးသွားတယ်။  ရိုးရှင်းပြီး ကြားကနေ လမ်းပြောင်းပေးတဲ့သူ စီစဥ်ပေးတဲ့သူမလိုတဲ့အခါမျိုးတွေမှာ သူက သုံးလို့အဆင်ပြေဆုံးပဲ။ သူ့ structure မှာက broker နဲ့ processor ဆိုပြီး ၂ ခုပဲရှိတယ်။ broker က event flowဖြစ်ဖို့နဲ့  processor က mediator မှာလိုပဲ တကယ့် business logic process ကို လုပ်ဆောင်ပေးတဲ့သူ။ ပုံ ၃ ကိုကြည့်ပါ။ သူ့ရဲ့ topologyက လက်ဆင့်ကမ်းအပြေးပြိုင်ပွဲလိုမျိုး မြင်ယောင်ကြည့်ရင် ပိုပြီး နားလည်ရလွယ်မယ်ထင်တယ်။ အပြေးအားကစားသမားတယောက်က တခြားတယောက်ကို တုတ်တိုလေးကို လက်လှမ်းပေးရင်း ပြေးရင်းနဲ့ နောက်ဆုံးပန်းတိုင်ထိ ဆင့်ကမ်းပေးသွားသလိုမျိုးပဲ event တခုကို processerတခုက တခုဆီ လှမ်းပေးရင်း ထပ်ပြီး အဲဒီ eventနဲ့ ပတ်သက်ပြီး လုပ်စရာ processမရှိတော့တဲ့အထိ အဆုံးသတ်ထိ အလုပ်လုပ်သွားတဲ့ပုံစံမျိုးပေါ့။

<figure><img src=".gitbook/assets/image (2).png" alt=""><figcaption><p>Figure 2-2 Event-driven architecture broker topology</p></figcaption></figure>



