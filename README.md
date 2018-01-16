# STEPBible-Data
Data created for www.STEPBible.org, licensed by Tyndale House Cambridge (CC BY-NC-ND 4.0)

# This public licence allows you to:
* Include any part of STEPBible-Data in free software or free publications without requesting permission 
  - (Though we'd love to hear from you about your project when you make it available.)
* Request permission if your project is not free. A reasonable request is unlikely to be refused. 
* Download the data and reformat it for your application, without changing the data
* Send any proposed corrections to TyndaleStep@gmail.com
  - (Please do not implement any change to the data till Tyndale scholars have verified it.) 
* Refer others to this repository as the source of the data. Please do not redistribute it yourself.
  - (Updates or corrections are easier to implement when the data is distributed from a single source)
  
And you should: 
* Credit it to "Tyndale House, Cambridge" linked to www.TyndaleHouse.com,   
        and to "STEP Bible" linked to www.STEPBible.org

# Tyndale House is an international Biblical Research Institute 
About 50 scholars at a time work at Tyndale House, often from more than a dozen countries. Most work on private research, and some work on special projects for Tyndale House, such as this one. 
The data in this repository is created and curated collaboratively by Tyndale scholars, directed by David Instone-Brewer with the oversight of Peter Williams, and by their successors. 

The repository aims to provide reliable and freely usable data for studying the Bible without any denominational or doctrinal bias. Much of the data is derivative from other publically licenced sources, and has been compared with other non-public sources so that differences can be checked by Tyndale scholars. Corrections and proposed updates are welcomed - please send them to TyndaleStep@gmail.com for checking.

# Data format 
Data is in plain unicode text (UTF-8) with tabs separating fields so it can be loaded into any text editor or spreadsheet. 

In most data sets, each line has identical fields, so an end-of-line marks the end of a record.
For some data (e.g. ProperNames), a record can consist of multiple lines and the record starts with "$". In this case the first line has data which applies to each succeeding line in the record. 

* Hebrew merged glyphs are separated and normalised in the order: consonant; sin/shin dot; dagesh; vowel; metheg/raphe; accents
  - Glyphs NOT used for Hebrew include: װ ױ ײ ﭏ ײַ שׁ שׂ שּׁ שּׂ אַ אָ אּ בּ גּ דּ הּ וּ זּ טּ יּ ךּ כּ לּ מּ נּ סּ ףּ פּ צּ קּ רּ שּ תּ וֹ בֿ כֿ פֿ ﬠ ﬡ ﬢ ﬣ ﬤ ﬥ ﬦ ﬧ ﬨ 

* Greek glyphs used are  ; · . , ᾽ ά ά ὰ ᾷ ᾷ ἀ Ἀ Ἀ ἁ Ἁ ἄ ἄ Ἄ Ἄ ἅ ἂ ἂ ἅ ἃ ἃ ᾶ ᾳ ἆ ἆ έ έ ὲ ἐ Ἐ Ἐ ἑ Ἑ ἔ Ἔ ἒ ἕ ἕ Ἒ Ἕ Ἕ ἓ ἓ ή ή ὴ ῇ ῇ ἠ Ἠ Ἠ ἡ Ἡ ἤ ἤ Ἤ Ἤ ἢ ἢ ἥ ἥ Ἢ Ἢ ἣ ἣ ᾖ ᾖ ᾗ ᾗ ᾗ ῆ ῃ ῄ ῄ ἦ ἦ Ἦ Ἦ ἧ ἧ ᾐ ᾐ ᾑ ᾔ ᾔ ί ί ὶ ϊ ΐ ΐ ΐ ῒ ῒ ἰ Ἰ Ἰ ἱ Ἱ ἴ ἴ Ἴ Ἴ ἵ ἵ Ἵ Ἵ ἳ ἳ ῖ ἶ ἶ ἷ ἷ ό ό ὸ ὀ Ὀ Ὀ ὁ Ὁ ὄ ὄ Ὄ Ὄ ὅ ὅ ὂ ὂ Ὅ ὃ ὃ Ὃ Ὃ Ὃ ῥ Ῥ ̔Ρ ύ ύ Ύ ὺ ϋ ΰ ΰ ΰ ῢ ῢ ὐ ὑ Ὑ ὔ ὔ ὒ ὒ ὕ ὕ ὓ ὓ ῦ ὖ ὖ ὗ ὗ ώ ώ ὼ ῷ ῷ ὠ Ὠ ὡ Ὡ ὤ ὤ Ὤ ὢ ὢ ὥ ὥ Ὥ Ὥ ᾦ ᾧ ᾧ Ὧ ᾯ ᾯ ῶ ῳ ῴ ῴ ὦ ὦ Ὦ ὧ ὧ ὧ ᾠ ᾠ 
  - Glyphs NOT used for Greek include: ; ' ᾿ ` ῾ ’ ‘ ‛ ′ ΄ ʹ̛̀́̓̒̓̔̕ ʹ ʻ ʼ ʽ ʾ ʿ ˈ ˊ ˋ ' ` ´ o ά ὰ ᾷ ἀ Ἀ ἁ Ἁ ἄ Ἄ ἅ ἂ ἃ ᾶ ᾳ ἆ έ ὲ ἐ Ἐ ἑ Ἑ ἔ Ἔ ἕ Ἕ ἓ ή ὴ ῇ ἠ Ἠ ἡ Ἡ ἤ Ἤ ἢ ἥ Ἢ ἣ ᾗ ῆ ῃ ῄ ἦ Ἦ ᾖ ἧ ᾐ ᾑ ᾔ i ί ὶ ϊ ΐ ῒ ἰ Ἰ ἱ Ἱ ἴ Ἴ ἵ Ἵ ἳ ῖ ἶ ἷ ό ὸ ὀ Ὀ ὁ Ὁ ὄ Ὄ ὅ ὂ Ὅ ὃ Ὃ ῥ Ῥ ύ ὺ ϋ ΰ ῢ ὐ ὑ Ὑ ὔ ὕ ὒ ὓ ῦ ὖ ὗ ώ ὼ ῷ ὠ ὡ Ὡ ὤ Ὤ ὢ ὥ Ὥ ᾦ ᾧ ᾯ ῶ ῳ ῴ ὦ Ὦ ὧ Ὧ ᾠ ϛ 
