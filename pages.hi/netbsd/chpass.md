# chpass

> उपयोगकर्ता डेटाबेस जानकारी जोड़ें या बदलें, जिसमें लॉगिन शेल और पासवर्ड शामिल हैं।
> और देखें: `passwd`।
> अधिक जानकारी: <https://man.netbsd.org/chpass>।

- वर्तमान उपयोगकर्ता के लिए इंटरैक्टिव रूप से एक विशिष्ट लॉगिन शेल सेट करें:

`su -c chpass`

- वर्तमान उपयोगकर्ता के लिए एक विशिष्ट लॉगिन [s]शेल सेट करें:

`chpass -s {{शेल/का/पथ}}`

- एक विशिष्ट उपयोगकर्ता के लिए एक लॉगिन [s]शेल सेट करें:

`chpass -s {{शेल/का/पथ}} {{उपयोगकर्ता_नाम}}`

- `passwd` फ़ाइल प्रारूप में एक उपयोगकर्ता डेटाबेस प्रविष्टि निर्दिष्ट करें:

`su -c 'chpass -a {{उपयोगकर्ता_नाम:encrypted_password:uid:gid:...}} -s {{उपयोगकर्ता_नाम}}' {{उपयोगकर्ता_नाम}}`

- केवल [l]स्थानीय पासवर्ड फ़ाइल को अपडेट करें:

`su -c 'chpass -l -s {{शेल/का/पथ}}' {{उपयोगकर्ता_नाम}}`

- मजबूरन डेटाबेस [y]P पासवर्ड डेटाबेस प्रविष्टि बदलें:

`su -c 'chpass -y -s {{शेल/का/पथ}}' {{उपयोगकर्ता_नाम}}`
