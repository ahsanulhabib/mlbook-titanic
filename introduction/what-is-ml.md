# ৩.১. মেশিন লার্নিং জিনিসটা কি?

> Machine learning is an application of artificial intelligence \(AI\) that provides systems the ability to automatically learn and improve from experience without being explicitly programmed.
>
> Machine learning focuses on the development of computer programs that can access data and use it learn for themselves.

আচ্ছা, কম্পিউটার ব্যবহার করি কেন আমরা? আমাদের কাজে সহায়তা দেয়ার জন্য। প্রসেস 'অটোমেট' করার জন্য। ঠিক তো? আমরা কিছু প্রোগ্রাম লিখি, আর কম্পিউটার সেই প্রোগ্রামের আদলে কাজটা করে দেয় আমাদের। এই প্রোগ্রামিংটাকে আমরা বলতে পারি এক ধরনের 'অটোমেশন'। আর, প্রোগ্রামিংটা করে দেয় কে? কে আবার, মানুষ।

এদিকে প্রোগ্রামিং করাও যেমন কষ্ট, আবার প্রোগ্রামিং করার মানুষও পাওয়া যায় না দরকার মতো। তাহলে কি করা? মানুষের জায়গায় ডাটাই করে দেবে সেই প্রোগ্রামিং। মেশিন লার্নিং হচ্ছে কম্পিউটারকে সেই প্রোগ্রামিং শেখানোর মত। ডাটাই বলে দেবে কিভাবে কম্পিউটার নিজেকে প্রোগ্রাম করবে। প্রোগ্রামিংকে যদি 'অটোমেশন' হিসেবে ধরে নেই, তাহলে মেশিন লার্নিং হচ্ছে ওই 'অটোমেশন' এর প্রসেসকে অটোমেট করার সিস্টেম।

বুঝলাম না সংজ্ঞাটা।

আচ্ছা, ছবি দেবো কি একটা?![](../.gitbook/assets/def.png)

**ছবি: সনাতন প্রোগ্রামিং আর মেশিন লার্নিং এর মধ্যে পার্থক্য** 

কৃত্তিম বুদ্ধিমত্তার একটা ভাগ হচ্ছে মেশিন লার্নিং। এটা এমন একটা অ্যাপ্লিকেশন যা কয়েকটা জিনিস করে:

১. আপনার সিস্টেমকে একটা দক্ষতা দেয় নিজে থেকে শেখার

২. সিস্টেমের শেখাটা আসে "অভিজ্ঞতা" অর্থাৎ পুরানো ডাটা থেকে

৩. এই শেখাটা কিন্তু আলাদা করে তাকে "প্রোগ্রামিং" করে দেয়া হয়নি

একটু ঘুরপাক খেয়ে আসি অন্যভাবে। এই ‘মেশিন লার্নিং’ নিয়ে। আবারো বলছি - কি জিনিস এটা? মানুষ যাই আবিস্কার করেছে, তা করেছে প্রকৃতির সৃষ্টিকে দেখে। বাঁজপাখির ওড়া দেখে উড়ুক্কুযান, বাদুড় দেখে সাবমেরিনের ‘সোনার’ - আরো কতো কি! তবে, মানুষ মানেই অলস। \*\* আমার মতো কিছুটা। অন্যকে দিয়ে কাজ করাতে ওস্তাদ। তক্কে তক্কে ছিলো বটে। যন্ত্রকে দিয়ে কাজ করানো নিয়ে। মানুষ ‘ইন্সট্রাকশন’ দেয়, যন্ত্র কাজ করে। ঠিক আছে সবই। যেমন - প্রোগ্রাম লেখে মানুষ, কাজ করে বেকুব যন্ত্র। তো, প্রোগ্রাম লেখাও তো কষ্টের। কি করা যায়?

মানুষ তাকালো নিজের দিকে। আচ্ছা, নিজে শেখে কিভাবে? অবশ্যই অভিজ্ঞতা থেকে। যেমন, ছোটবেলা থেকে দেখে এসেছি নীল চোখের গুলটু মার্কা ছোট্ট প্রাণীটা আসলে বিড়াল। বাচ্চা বয়সে প্রথম প্রথম ওই বিড়াল দেখে ভয় পেলেও মা শিখিয়েছেন জিনিসটা কি। বইয়ের ছবি দেখিয়ে। শত বিড়ালের শত ধরণের আকৃতি/ছবি দেখে মাথায় ঢুকে গেছে একটা জিনিস। যে রঙেরই হোক, শুয়ে বা দাড়িয়ে থাকুক - সেটা বিড়াল। এটাই অভিজ্ঞতা অর্জন। মানুষের জন্য।

তো, অভিজ্ঞতা দেয়া যায় কিভাবে? মানে যন্ত্রকে? ঠিক বলেছেন। ডাটা দিয়ে। একটা দুটো নয়, ঘটে যাওয়া হাজারো ডাটা দিয়ে। ‘বিড়াল’ লিখুন বাংলায়। গুগল ইমেজে। ঠিক ঠিক খুঁজে নিয়ে আসবে কালো, সাদা, শোয়া, দাড়ানো, দাত ক্যালানো বিড়াল। বাংলায় লিখুন ‘কালো বিড়াল’, খুঁজে নিয়ে আসবে কালো সব নীল চোখা বিড়াল। আরে, শিখলো কিভাবে? শিখিয়েছে মানুষ, যেভাবে শেখে নিজে। হাজারো বিড়ালের ‘ক্যারিক্যাচার’ ছবি দেখিয়ে যন্ত্রকে বলা হয়েছে এটাই বিড়াল। শিখবে না মানে? ওর বাপ শিখবে। এটাই ‘ট্রেনিং’ ডাটা। যন্ত্রের জন্য। আরো পোক্ত করতে দেখানো হলো দেশী বিদেশী বিড়ালের ছবি। মিলিয়নে মিলিয়নে। ভুল হবার নয় আর। দেখলেই হলো খাটের নিচের অন্ধকারে থাকা বিড়ালের চোখ? বলে দেবে ঠিক ঠিক।

মনে আছে প্রফেসর অ্যান্ড্রু ইংয়ের কথা? আমার প্রিয় একজন মানুষ। স্ট্যানফোর্ডের এই প্রফেসর ২০১২তে তৈরি করেছিলেন বিশাল একটা কোর্স। ‘মেশিন লার্নিং’ দুনিয়ায় এটা এখনো একটা নামকরা কোর্স। ফ্রি হওয়াতে এনরোল করেছে হাজার হাজার মানুষ। হেলিকপ্টার ওড়ানো নিয়ে একটা উদাহরণ দিয়েছিলেন ওখানে। প্রথমে বিশ্বাস করিনি কথাটা। বলেছিলেন, ‘অটোনমাস’ হেলিকপ্টারটাকে ঠিকমতো ওড়ানো যাচ্ছিলো না প্রথম দিকে। মানে, মানুষের তৈরি প্রোগ্রাম দিয়ে। ভিডিওতেও দেখা গেলো পাগলের মতো উড়ছে জিনিসটা। পরে বুঝতে পারলাম, ঠিক মতো উড়তে হলে - তাকে শিখতে হবে নিজে নিজে। অভিজ্ঞতা নিয়ে। মানে, হাঁটি হাঁটি পা ফেলার মতো উল্টাপাল্টা উড়ে। ডানে বামে বাড়ি খেয়ে। হেলিকপ্টার তো মানুষ না, ওই হেলিকপ্টারকেই নিজে থেকে উড়ে দরকারি ‘এরর কারেকশন’ দিতে হবে ঠিকমতো। শিখতে হবে নিজেকে। কোন ‘টর্কে’ কি রোটেশন হবে, কখন স্পিড বাড়াতে কমাতে হবে সেটা ‘এক্সপেরিয়েন্স’ না করলে কারেকশন করে নেবে কিভাবে? এভাবেই এলো যন্ত্রের অভিজ্ঞতা নেবার গল্প।

_\*\* স্বাতীর ভাষায় আমি নাকি পুরোই যন্ত্র। চামড়া ছিলে গেলে নাকি স্টেইনলেস স্টিল পাওয়া যাবে। বয়স বাড়ছে। দিন দিন মানুষ হচ্ছি। আমার ধারণা, ‘অ্যাক্যুরেসি’ বাড়ছে মেশিন লার্নিংয়ে। আর তাই মানুষ হচ্ছি সময়ের সাথে_

_\* আমার স্ত্রী স্বাতী_ 

