# 5 Space-based Architecture

web-base business application အများစုဟာ တူညီတဲ့ request flowနဲ့သွားကြပါတယ်။ browser ကနေ request ရလာမယ်။ web server ဆီကိုရောက်မယ်။ အဲ့ကနေ application server၊ နောက်ဆုံး Database serverဆီကိုရောက်မယ်။ ဒီလို  patternတွေက users အနည်းငယ်အတွက် တော့ အဆင်ပြေနေပါလိမ့်မယ်။ သုံးတဲ့သူများလာရင်တော့ bottleneck issuesတွေစဖြစ်လာပါပြီ။ အဲဒါကို ပြေလည်ဖို့အတွက်ဆိုရင်တော့ web serverတွေကို scale outလုပ်ပြီး ဖြေရှင်းလေ့ရှိကြပါတယ်။ ဒီနေရာမှာ web-server တွေကို scale out လုပ်တာဟာ လွယ်ကူ ရိုးရှင်းပေမဲ့၊ တဆင့်တက်ပြီး applicaiton serverတွေထိ scale out လုပ်ဖို့လိုလာရင်တော့ ထင်သလောက် မရိုးရှင်းနိုင်တော့ပါဘူး။ နောက်ဆုံးအဆင့် database serverထိ scale out လုပ်ရတော့မယ်ဆိုရင် costကတော့ မသက်သာပါဘူး။ သူကအခက်ဆုံးပါပဲ။

တပြိုင်နက် သုံးစွဲသူများတဲ့ high-volume applicationတွေမှာဆိုရင် တပြိုင်နက် transaction ဘယ်လောက်ထိ လုပ်ပေးနိုင်တယ်ဆိုတဲ့ နောက်ဆုံး limitဆိုတာရှိတတ်ပါတယ်။ caching တွေ database scaling productsတွေက ဒီပြဿနာကို ဖြေရှင်းကောင်းဖြေရှင်းနိုင်ပေမဲ့ သာမန် applicationတခုကို loads အလွန်အကျွံ များတဲ့အခါမျိုးမှာ တော့ scale out လုပ်ဖို့ ဆိုတာ ခက်ခဲတဲ့ အခြေအနေတခုပါ။ Space-based architecture patternဟာ concurrency နဲ့ scalabilityနဲ့ဆိုင်တဲ့ပြဿနာတွေကို ဖြေရှင်းဖို့ design လုပ်ထားတဲ့ patternတခုပါ။ မမျှော်မှန်းနိုင်လောက်တဲ့ထိ userတွေများလာခဲ့ရင်တော့ ဒီpatternက အသုံး၀င်ဆုံးဖြစ်ပါတယ်။ ဒီလိုမျိုးအခြေနေမှာ database ကိုscale out လုပ်တာမျိုး cachingတွေနဲ့ ဖြေရှင်းဖို့ကြိုးစားတာထက်စာရင်တော့ architecture နည်းနဲ့ဖြေရှင်းတာက ပိုကောင်းတဲ့ ချဥ်းကပ်မှုတခုဖြစ်ပါလိမ့်မယ်။



