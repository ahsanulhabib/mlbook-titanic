### ডিসিশন ট্রি, কাহিনী কি?

---

এ পর্যন্ত আমরা যা যা করেছি - তার সব কিছুই করেছি হাতে কলমে, ছোট ছোট অংকের অনুপাত দিয়ে, অনেক ঝামেলা করে। প্রতিটা দরকারি ‘ভ্যারিয়েবল’ নিয়েছি আলাদা করে, সেগুলো থেকে খুঁচিয়ে খুঁচিয়ে বের করছি এর ভেতরের সাবসেট আর তার অনুপাত। বড় ডাটাসেটগুলোকে ভাগ করে ফেলেছিলাম ছোট ছোট সাবসেটে। ছোট্ট সাবসেটগুলোতে দরকারি ডাটা চোখে পড়ে ভালোভাবে। মডেলের একুরেসি আনার জন্য আমাদের এই ডাটাসেটকে ভাগ করতে হবে আরও ছোট ছোট সাবসেটে। তখন দেখা যাবে প্রতিটা ভ্যারিয়েবলের মধ্যে সম্পর্কটা কত নিবিড়। এই সম্পর্কগুলো আরো ভালো বোঝা যাবে যখন সাবসেটগুলো কথা বলবে নিজেদের ভেতর।

আসল কথা হচ্ছে আমরা অলস। আচ্ছা, ভুল বলেছি, আমি অলস। এই প্রতিটা ডাটাসেট ধরে ধরে ছোট ছোট সেটে ভাগ করে অনুপাতগুলো খুঁজে খুঁজে বের করার মত কর্মঠ আমি নই। আমি ক্লিক করব - আর হয়ে যাবে কাজ। সে কারণেই তো শিখছি মেশিন লার্নিং। ও বলে দেবে ডাটা দেখে - আমি তো বসম্যান। তাই হচ্ছে কিন্তু আমাদের ডাটা সাইন্স গ্যালাক্সিতে। অনেক চমৎকার জিনিস আসছে। তবে, বেসিক না জানলে কিছুই করা যাবে না এখানে।

তাই শুরুতেই খুবই সাধারণ এবং আমার প্রিয় একটা অ্যালগরিদম নিয়ে কাজ করব এখানে। আমি নই, যারা মেশিন লার্নিংয়ে নতুন বা পুরাতন সবাই শুরু করে এই ‘অ্যালগো’ দিয়ে। এটা আসলে অ্যালগরিদম নয় বরং সিদ্ধান্ত নেওয়ার একটা ডিসিশন ট্রি। শুধু মেশিন লার্নিং নয় সব কিছুতেই লাগে এই সিদ্ধান্ত গাছ বা ডিসিশন ট্রি। ভাবুন, আমরা যে কোনো কাজ করতে গেলে মনে মনে একটা “ট্রি” এঁকে ফেলি। মানে, এদিকে যাবো না ওদিক যা বো। কোনটা সুবিধা হবে? ব্যাপারটা এরকম যে আমরা যদি কোনো সিদ্ধান্ত নিতে চাই, তাহলে কোনো একটা ইনপুটের ওপর ভিত্তি করে দরকারি ফ্লো-চার্টের ডানে অথবা বামে যাই।![](/assets/tree1.png)

মনে করুন - একটা গাছেরই কথা। আমরা যখন একটা গাছের ওপরে ওঠার চেষ্টা করি, প্রথমেই ধরি ওই গাছের গুঁড়িটাকে। গুঁড়ি শেষে আমাদের সামনে পড়ে গাছের কয়েকটা কান্ড। কান্ড বেয়ে ওপরে উঠলে সামনে পড়ে সেই কান্ডের শাখা প্রশাখা। আমাদের সিদ্ধান্ত সেরকম কিছুটা। প্রথমে আসে বড় সিদ্ধান্ত, তারপরে আসতে থাকে মাঝারি সিদ্ধান্ত, এরপর ছোট ছোট সিদ্ধান্ত। গাছটাকে যদি উল্টো করে ধরি, তাহলে সিদ্ধান্তের শেষ সীমানায় পৌঁছাতে গেলে ‘নেভিগেট’ করতে হবে সেই গুড়ি দিয়ে - শুরুতে। তখন গুঁড়ির পরে আসবে কান্ড, তারপর সেগুলোর ছোট ছোট শাখা প্রশাখা।

চলুন ব্যাপারটাকে হিসেব করি টাইটানিকের ডাটাসেট নিয়ে। “train” ডাটাসেট নিয়ে কি করেছিলাম প্রথমে? বের করতে চেষ্টা করেছিলাম কে বেঁচে আর মারা গিয়েছিলেন, তাইনা? সেটাই হচ্ছে এই গাছের গুঁড়ি। এরপর এলো সেই বেঁচে যাওয়ার মধ্যে কতজন পুরুষ এবং মহিলা, তাইতো? সেগুলো হচ্ছে ওই গাছের কান্ড। নিচের একটা ছবি দেখি বরং। ছবিটা কিভাবে এলো সেটা নিয়ে মাথা৫ ঘা মাই পরে। পুরো ডাটাসেটে দেখা গেল মারা গিয়েছেন বেশিরভাগ। প্রতিটা মানুষের একটা ভোটের হিসেব করলে বেশির ভাগ ভোট পড়বে শূন্যের ঘরে।

আপনারা তো জানেন আমাদের ফলাফল যেটা বাইনারি ক্লাসিফিকেশনে “০”। বাঁচা ১, মরা ০, তাইতো? ১০০% ডাটা সেটে বেঁচেছেন মাত্র ৩৮%। এর অর্থ হচ্ছে মারা গিয়েছেন প্রায় ৬২ শতাংশ। গুঁড়ি থেকে এবার আসি কাণ্ডে। তখন প্রশ্ন আসবে, আপনি পুরুষ না মহিলা? পুরুষ হলে ফলাফল আগের মত ‘০’। কারণ - পুরুষের ভোটের ফলাফল মৃত্যুর ঘরে বেশি। ওই ৬৫% প্যাসেঞ্জারের মাত্র ১৯% বেঁচেছেন। ব্যাপারটা না বুঝলে আবার দেখুন ছবিটা। আমরা দুই নম্বর ঘরের কথা বলছি। ১ নম্বর ঘর কথা বলেছে কে বেঁচে গিয়েছিলেন আর কে মারা গেছেন। সেখানেও ভোটের সংখ্যায় “০” বেশি। দুই নম্বর ঘরেও ভোটের সংখ্যা “০” বেশি যেহেতু সবাই পুরুষ। তিন নম্বর ঘর - ২ নম্বর ঘরের পুরোপুরি উল্টো। এখানে ভোট পড়েছে “এক” এ বেশি। ৩৫ শতাংশ মহিলাদের মধ্যে ৭৩% মহিলারাই বেঁচে গেছেন। এজন্য এখানকার ভোটের ঘর “এক” দিয়ে পূর্ণ।

![](/assets/tree.png)

বুঝলাম, বোঝেননি কিছু। চলুন ফিরে আর ষ্টুডিওতে।

এই যে বার বার সিদ্ধান্ত পার্টিশন করছি ডাটার অনুপাতের ওপর - এটাই কিন্তু একটা রিকার্সিভ পার্টিশনিং মেথড। এটা পেয়েছি আমরা ১৯৮৪ সালে - CART হিসেবে। গুগল করলেই বুঝবেন কি সাংঘাতিক জিনিস এটা। পরিসংখ্যানের জেনারেলাইজড লিনিয়ার মডেলের বিকল্প হিসেবে এসেছে এই রিকার্সিভ পার্টিশনিং ট্রি। আর এর প্যাকেজটার নাম হচ্ছে rpart\(\) যা ফাংশন হিসেবে চলে। এখানে মাথা খারাপ করা চলবে না - না বুঝলে আমাকে বলুন আমি বলবো হাজারো বার নতুন গল্প দিয়ে।

### ভিজ্যুয়ালাইজেশন, দেখাতেই বিশ্বাস

---

ঝামেলা চুকিয়ে ফেলি কিছু প্যাকেজ নিয়ে একসাথে। ক্স\`ইনস্টল করে নেই কিছু প্যাকেজ। rattle আর rpart.plot। ওমা, প্লট করতে হবে না? ভিজ্যুয়ালাইজেশন যে দরকার! একটু বসতে হবে আপনাকে। কিছু ডিপেন্ডেন্সি প্যাকেজও  লোড এক সাথে। ভার্সন কনফ্লিক্ট হলে gtk+ প্যাকেজ ইনস্টল হতে চাইবে এর সাথে।

install.packages\('rattle'\)

install.packages\('rpart.plot'\)

install.packages\('RColorBrewer'\)

শুরুতে লোড করি rpart\(\) লাইব্রেরিকে।

library\(rpart\)

library\(rattle\)

library\(rpart.plot\)

library\(RColorBrewer\)

শুরুতেই তৈরি করি একটা জেন্ডার মডেল। ভ্যারিয়েবল হিসেবে নেই শুধুমাত্র Sex, আগের ছবি কিভাবে এসেছে সেটা বোঝানোর জন্য। পরের লাইনটা দরকার বুঝতে। ছবিতে।

mytree1 &lt;- rpart\(Survived ~ Sex, data=train, method="class"\)

fancyRpartPlot\(mytree1\)

![](/assets/Rplot.png)

পরের মডেলে ভ্যারিয়েবল হিসেবে নেই বয়স আর ক্লাস \(Pclass\)কে। মাত্র দুটো ভ্যারিয়েবলকে। ভেতরে বোঝার সুবিধার্থে।

mytree1 &lt;- rpart\(Survived ~ Sex, data=train, method="class"\)

fancyRpartPlot\(mytree1\)
