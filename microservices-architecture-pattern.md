# 4 Microservices Architecture Pattern

Microservices ကတော့ ခုလက်ရှိအသုံးများနေတဲ့  monolithic applicationနဲ့ service-oriented architecure တွေအတွက် evolutionary pathတခုအနေနဲ့ တခြားရွေးချယ်စရာ architectureတခုပါ။ ခုထိလည်း တိုးတက်ပြောင်းလဲနေဆဲဖြစ်တာကြောင့် IT industryမှာလည်း implementလုပ်ပုံလုပ်နည်း ဒီpatternအကြောင်း အဓိပ္ပါယ်အမျိုးမျိုးနဲ့ ပုံဖော်နေကြတုန်းပါပဲ။&#x20;

အရင် patternတွေမှာ topology တွေ implementation styleတွေ ဘယ်လိုပဲ ရှိရှိ၊ သူတို့တွေထဲမှာ တူညီတဲ့ conceptသဘောတရားတွေ အများကြီးရှိပါတယ်။ အဲဒီထဲက တခုကတော့ သီးသန့် unit တခုအနေနဲ့ ခွဲထုတ်တဲ့ အယူအဆပါ။  microservices မှာ componenet တခုစီဟာ သီးခြား deployလုပ်နိုင်တဲ့အတွက် deploy လုပ်ရာမှာ လွယ်ကူတယ်၊ scalability ကောင်းတယ်။ decoupling ဖြစ်တယ်။ ပြင်ဆင်ရလွယ်ကူမယ်။ အဲဒီcomponentတွေဟာ single purpose functionတွေလည်းဖြစ်နိုင်တယ်  component တခုစီဟာ တခုထက်မကတဲ့ modules တွေ ပေါင်းထားတာလည်းဖြစ်နိုင်တယ်။ ကြီးမားတဲ့ ရှုပ်ထွေးတဲ့ applicationတွေတည်ဆောက်တဲ့အခါမှာ အဲလိုမျိုး service component တွေကို မှန်ကန်တဲ့ အထားအသိုနဲ့ တည်ဆောက်ဖို့ အရေးကြီးပါတယ်။

<figure><img src=".gitbook/assets/image (4).png" alt=""><figcaption><p>Figure 4-1 Basic Microservice architecture pattern</p></figcaption></figure>

နောက်ထပ် main conceptတခုကတော့ distributed ဖြစ်ခြင်းပဲဖြစ်တယ်။ componentတခုစီဟာ fully decoupled ဖြစ်ကြတယ်။ တခုနဲ့တခု access လုပ်ဖို့ဆိုရင် REST, JMS, AMQP, etc အစရှိတဲ့ remote access protocolတွေကိုသုံးပြီး ချိတ်ဆက်ကြပါတယ်။ ဒါဟာလည်း scalability နဲ့ deploymentအတွက် အထောက်အကူပြုစေပါတယ်။

ဒီarchitectureက တခြားသောarchitecture patternတွေမှာတွေ့ရလေ့ရှိတဲ့ ပြဿနာတွေကို ဖြေရှင်းဖို့ နည်းလမ်းရှာဖွေရာကနေ ဖြစ်ပေါ်လာတဲ့ patternတခုဖြစ်တယ်။ အဓိကအားဖြင့် layered architectureအသုံးပြုထားတဲ့ monolithic applications နဲ့ service oriented architecture patternနဲ့တည်ဆောက်ထားတဲ့ distributed applicationတွေကနေ evolution လုပ်ပြီး ဖြစ်ပေါ်လာတဲ့ patternတခုဖြစ်တယ်။ monolithic applicationမှာဆိုရင်  tightly coupled ဖြစ်တတ်တဲ့အတွက် microservice patternဆီပြောင်းလဲနိုင်ခဲ့ရင် continuous delivery (CD)ကိုပိုပြီးလွယ်ကူသွားစေတယ်။ tightly coulple ဖြစ်တဲ့ componentတွေ ဟာ deploy လုပ်ရာမှာ၊ testing လုပ်ရာမှာ၊ customizeလုပ်တဲ့အခါတွေမှာ အချိန်ကြာနိုင်တယ်။ ပြီးတော့ IT company အများစုမှာတွေ့ရတတ်တဲ့ monthly deploymentတွေမှာပဲ လုံးလည်လိုက်နေနိုင်တယ်။ တခုပြင်တာနဲ့ အကုန်လိုက်ပြီး deployချ ဖို့လိုနေတာမျိုးပေါ့။ microservice ကတော့ တစိတ်တပိုင်း ပြင်ဆင်ချင်တဲ့အခါ အဲဒီ ပြင်ချင်တဲ့ componentကိုပဲ deployချ၊ testingလုပ်ရုံပါပဲ။ အရမ်းရိုးရှင်းပြီး managementလုပ်လို့ ကောင်းပါတယ်။&#x20;

Service-oriented architecture (SOA) patternကနေပြီးတွေ့ရလေ့ရှိတဲ့ issuesတွေဟာလည်း microservice patternဆီကို ပြောင်းလဲဖို့ ဦးတည်စေတဲ့အကြောင်းအရာတခုဖြစ်ပါသေးတယ်။ SOA patternဟာ ITနယ်ပယ်မှာ အရမ်းကို အသုံး၀င်ပြီးတော့ business goal အလိုက် service levelတွေနဲ့ မတူထူးခြားတဲ့ စွမ်းဆောင်ရည်တွေရှိပါတယ်။ ဒါပေမဲ့ သူ့ကို အသုံးပြုတဲ့အခါမှာ တခါတခါ ရှုပ်ထွေးခက်ခဲပြီး manageလုပ်ရ မလွယ်ကူတာမျိုး၊ နားလည်ရမလွယ်ကူတာမျိုးကြောင့် တော်တော်များများ applicationတွေအတွက်က မလိုအပ်ဘဲ အလွန်အကျွံ cost များနေတတ်ပါတယ်။ microservice patternကတော့ SOA ရဲ့ ရှုပ်ထွေးတဲ့ အပိုင်းတွေ (ဥပမာ orchestrationလိုမျိုး centerကနေ စီမံပေးဖို့ လိုအပ်နေတာမျိုး၊ dependencyတွေလျော့ချပစ်တာမျိုး) ကိုဖယ်ဖျက်ပြီး ရှင်းလင်းတဲ့ access တွေ connectivityတွေနဲ့ အစားထိုးပြီး ပြောင်းလဲ ပေးနိုင်ပါတယ်။

### Topologies

ဒီလိုဆို microserviceကို ဘယ်လို implement လုပ်မလဲ အသုံးချမလဲ ဆိုတော့ သူ့မှာ နည်းလမ်းပေါင်းများစွာရှိနေပြန်ပါသေးတယ်။ အဲဒီထဲကမှ အသုံးများဆုံး ၃ ခုကတော့ API REST-based, Application REST-Based နဲ့ centralized messaging topologyပဲဖြစ်တယ်။

#### API REST-based Topology

API REST-based topology ဟာ individual service api တွေနဲ့ဖွဲ့စည်းထားတဲ့ websites တွေကိုဖန်တီးတဲ့အခါ အသုံး၀င်ပါတယ်။ သူ့မှာ သီးသန့်ဖြစ်တဲ့ ဘယ်component ဘယ်business logicကိုမှ မမီခိုတဲ့ functionsတွေနဲ့ဖွဲ့စည်းထားတဲ့ component တနည်းအားဖြင့် modulesတွေပါ၀င်ပါတယ်။ ဒီ components တွေဟာ ပုံမှန်အားဖြင့် တခုနဲ့တခု ဆက်သွယ်ချိတ်ဆက်တဲ့အခါမှာ REST-based interface ကိုသုံးနိုင်ပြီး deploymentကလည်း သီးခြားစီဖြစ်တဲ့ API layers တွေအနေနဲ့ မြင်တွေ့နိုင်ပါတယ်။ အဲလိုမျိုး single-purpose RESTful web services တွေနဲ့ဖွဲ့စည်းထားတဲ့ topology ကို Yahoo, Google တို့ Amazonတို့မှာ တွေ့ရတတ်ပါတယ်။

<figure><img src=".gitbook/assets/image (3).png" alt=""><figcaption><p>Figure 4-2 API REST-based Topology</p></figcaption></figure>

API REST-based နဲ့ application REST-based မှာ ဘာတွေကွာခြားသလဲဆိုရင် client requests တွေဟာ မြင်တွေ့နေကျ web-based တနည်းအားဖြင့် application screenဆီကနေ လာတာမဟုတ်ဘဲ ရိုးရှင်းတဲ့ API layerကနေတဆင့် လာတာဖြစ်ပါတယ်။

#### Application REST-based Topology

User-Interface layerဟာ သီးခြား web applicationတခုအနေနဲ့ deployလုပ်ထားပါတယ်။  သူကနေမှတဆင့် တခြားသော single-purpose service component တွေကို လှမ်းပြီး accessလုပ်တဲ့ ပုံစံမျိုးပါ။ ဒီနေရာမှာ service componentတခုစီ ဟာလည်း အထက်ကပြောထားသလိုပဲ သီးသန့် deploy လုပ်လို့ရတဲ့ testingလုပ်လို့ရတဲ့ API componentတခုစီဖြစ်ကြပါတယ်။ ဒီ topologyကိုတော့ small to medium sized applicationတွေအတွက် တတ်နိုင်သမျှ complexity လျော့ချစေဖို့အတွက် အသုံးပြုကြပါတယ်။&#x20;

<figure><img src=".gitbook/assets/image (7).png" alt=""><figcaption><p>Figure 4-3 Application REST-based Topology</p></figcaption></figure>

#### Centralized messaging topology

နောက်ထပ် အသုံးပြုများလေ့ရှိတဲ့ microservice topologyကတော့ centralized message topologyပဲဖြစ်တယ်။ သူက application REST-based နဲ့ ဆင်တူပြီး ကွာခြားတာတခုက componentsတွေကို လှမ်းဆက်သွယ်တဲ့အခါ REST ကို အသုံးပြုမဲ့အစား Active MQ, HornetQတို့လို message brokerကို အသုံးပြုတာဖြစ်တယ်။ သူ့ကို ရုတ်တရက်ကြည့်ရင် SOA လိုမျိုး နဲ့ ဆင်တူတယ်လို့ အထင်မှားနိုင်ပါတယ်။ ဒီမှာ အသုံးပြုမယ့် message brokerဟာ ကြားထဲက orchestrationတွေ transformationတွေ routing လုပ်ပေးမဲ့ componentတွေမလိုပါဘူး။ သူက component တွေချိတ်ဆက်ဖို့ အတွက်သက်သက်ပဲ message brokerကို အသုံးပြုတာဖြစ်ပါတယ်။ &#x20;

ဒီလို patternမျိုးကို application ကြီးတွေမှာ မြင်တွေရလေ့ရှိပါတယ်။  user interface နဲ့ componentsတွေကြားမှာ ပိုကောင်းမွန်တဲ့ transportation layerလိုအပ်တဲ့အခါ အသုံး၀င်ပါတယ်။ အထက်ကပြောထားခဲ့တဲ့ patternတွေထက် ပိုကောင်းတဲ့အားသာချက်ကတော့ queuing, asynchronous messaging, monitoring, error handling အပြင် load balancing နဲ့ scalability တွေမှာ အားသာပါတယ်။  Centralized Message Brokerတွေမှာတွေ့ရလေ့ရှိတဲ့ bottleneck issuesတွေကိုလည်း multiple brokerတွေအဖြစ် ခွဲပေးပြီး message တွေကို balancing လုပ်ခြင်းအားဖြင်လည်း ဖြေရှင်းပေးနိုင်ပါတယ်။ ဒါကြောင့်သူ့ကို SOA နဲ့ မှားမမြင်မိဖို့ အရေးကြီးပါတယ်။

<figure><img src=".gitbook/assets/image (2).png" alt=""><figcaption><p>Figure 4-4 Centralized Message Topology</p></figcaption></figure>

