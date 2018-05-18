# Tyndale STEPBible Data
Data created for www.STEPBible.org by [Tyndale House Cambridge](www.tyndale.cam.ac.uk)   
(CC BY-NC-ND 4.0 with additional specified relaxations)

# This licence allows...
This public licence allows you to: 
* **Include any part of STEPBible-Data in free software or free publications** without requesting permission    
  (Though we'd love to hear from you about your project when you make it available.)  
* **Request permission if your project is not free.** A reasonable request is unlikely to be refused.   
* **Download the data and reformat it for your application, without changing the data itself.**  
  (This specifically relaxes the ND restriction, as allowed by CC - see https://creativecommons.org/licenses/by-nd/4.0/legalcode)  
* **Send any proposed corrections** to TyndaleStepATgmail.com  
  (Please do not implement any change to the data till Tyndale scholars have verified it.)   
* **Refer others to this repository as the source of the data.**   
  Please do not redistribute it yourself. Updates or corrections are easier to implement when the data is distributed from a single source  
  
And you should:   
* **Credit it** to "Tyndale House, Cambridge" linked to www.TyndaleHouse.com,  
  and to "STEP Bible" linked to www.STEPBible.org    
  and refer to the source as tyndale.github.io/STEPBible-Data/

# Tyndale House is...  
Tyndale House is an international Biblical Research Institute. About 50 scholars at a time work there, often from more than a dozen countries. Most work on private research, and some work on special projects for Tyndale House, such as this one.   

The data in this repository is created and curated collaboratively by Tyndale scholars, directed by David Instone-Brewer with the oversight of Peter Williams, and by their successors.   

The repository aims to provide reliable and freely usable data for studying the Bible without any denominational or doctrinal bias. Much of the data is derivative from other publically licenced sources, and has been compared with other non-public sources so that differences can be checked by Tyndale scholars. Corrections and proposed updates are welcomed - please send them to TyndaleStepATgmail.com for checking.  

# Datasets  
Some of the following are already posted while others are still being checked. 
If you see data that you have need of which isn't yet available, please contact us and perhaps you can become part of the checking process.  

* **[TTESV - Tyndale Translation tags for ESV](https://github.com/tyndale/STEPBible-Data)**  
Tags for Greek & Hebrew Extended Strongs (compatible with original Strongs) for the translated text of the ESV.   

* **[TOTHT - Tyndale OT Hebrew Tagged text](https://github.com/tyndale/STEPBible-Data)**        
Based on Westminster with corrections from BHS (when it is correct) and from Tyndale scholars (when other two are wrong). All stems and affixes are tagged with extended Strongs to BDB, with context sensitive defs, and ETCBC morphology, including for ketive and qere readings.     

* **TANTT - Tyndale Amalgamated NT Tagged texts**     
A single NT Greek Text with all variants amalgamated from the major editions (SBLGNT, Treg, TR, Byz, WH, NA) based on SBLGNT+variants. Merged with 1st 4 centuries of MSS (from Bunning). One line per accented word form, each marked with the editions+MSS that include this form, so that deleting all other lines creates any of the individual texts with the option of including all variants. Each line is tagged lexically (extended Strong linked to LSJ) and morphologically (Robinson based on Tauber plus a few missing details) and context sensitive glosses.     

* **TOTGT - Tyndale OT Greek Tagged text**   
LXX text with later Ecclesiastical variants. The base text is Rhalfs with variants from the Apostolic Bible (based on Sixtine, Aldine and Complutensian texts). Both have been tagged to LSJ (compatible with extended Strongs) and most of morphology has been tagged (based on CCAT) but variant tagging need completing.    

* **[TBESH - Tyndale Brief lexicon of Extended Strongs for Hebrew](https://github.com/tyndale/STEPBible-Data)**     
Abridged BDB linked to extended Strongs (compatible with OpenScriptures and backwardly compatible with original Strongs)   

* **TFBDB - Tyndale Formatted full BDB lexicon**   
Full BDB formatted for easy reading (all bibliographic data hidden as hover-text) linked to extended Strongs (compatible with OpenScriptures and backwardly compatible with original Strongs)    

* **[TBESG - Tyndale Brief lexicon of Extended Strongs for Greek](https://github.com/tyndale/STEPBible-Data)**  
Abbott-Smith linked to extended Strongs for all Greek in NT & LXX (backwardly compatible with original Strongs).  

* **TFLSJ - Tyndale Formatted full LSJ lexicon**    
Full LSJ entries for all Bible words (LXX, Apoc & NT), formatted for easy reading (all bibliographic data hidden as hover-text) linked to extended Strongs (backwardly compatible with original Strongs).     

* **[TIPNR - Tyndale Individualised Proper Names with all References](https://github.com/tyndale/STEPBible-Data)**  
Every name in the Bible, linked to all Hebrew & Greek forms of that name and separated into individual people & places. Each form of the names for each individual includes exhaustive refs for where that individual is named with data of their spouses, siblings and offspring or the places' geolocation (based on OpenBible).    

* **TOTMM - Tyndale OT Manuscripts and Meanings**  
Translation, Hebrew form and witnesses for each variant that affects the meaning of the text, as determined by Barthélemy's UBS committee. Also, alternate meanings found in standard translations. Shown as alternate renderings of a base text (ESV 2011).    

* **TNTMM - Tyndale NT Manuscripts and Meanings**  
Translation, Greek form and witnesses up to 400 AD for each variant that affects the meaning of the text, as determined by the UBS apparatus. Also, alternate meanings found in standard translations. Shown as alternate renderings of a base text (ESV 2011).   

# Data format 
Data is in plain unicode text (UTF-8) with fields separated by tabs, so that they can be loaded into any text editor or spreadsheet.   
  
* **By default, datasets are one-line records**, so a Record ends with a NewLine, and each line has identical fields.  
  
* Some datasets have multi-line records. Records are separated by a line starting with "$". The first line is a Header with fields that apply to each subsequent subRecord line. SubRecord lines all start with a tab.   
For example, in the ProperNames dataset, the first line is a header with information about the type (individual, place, title etc) and other data. These details apply to each of the subsequent subRecords which contain fields for the specific tag, Hebrew/Greek, translation, and the list of references. So the Header effectively contains fields which belong to each of its subRecords and would be  identical for each of them if they were included on each line.   
  
* **Hebrew glyphs** are separated and normalised in the order:    
  consonant; sin/shin dot; dagesh; vowel; metheg/raphe; accents  
  - Glyphs NOT used for Hebrew include:  
  װ ױ ײ ﭏ ײַ שׁ שׂ שּׁ שּׂ אַ אָ אּ בּ גּ דּ הּ וּ זּ טּ יּ ךּ כּ לּ מּ נּ סּ ףּ פּ צּ קּ רּ שּ תּ וֹ בֿ כֿ פֿ ﬠ ﬡ ﬢ ﬣ ﬤ ﬥ ﬦ ﬧ ﬨ   
* **Greek glyphs** are normalised to include only:  
; · . , ᾽ ά ά ὰ ᾷ ᾷ ἀ Ἀ Ἀ ἁ Ἁ ἄ ἄ Ἄ Ἄ ἅ ἂ ἂ ἅ ἃ ἃ ᾶ ᾳ ἆ ἆ έ έ ὲ ἐ Ἐ Ἐ ἑ Ἑ ἔ Ἔ ἒ ἕ ἕ Ἒ Ἕ Ἕ ἓ ἓ ή ή ὴ ῇ ῇ ἠ Ἠ Ἠ ἡ Ἡ ἤ ἤ Ἤ Ἤ ἢ ἢ ἥ ἥ Ἢ Ἢ ἣ ἣ ᾖ ᾖ ᾗ ᾗ ᾗ ῆ ῃ ῄ ῄ ἦ ἦ Ἦ Ἦ ἧ ἧ ᾐ ᾐ ᾑ ᾔ ᾔ ί ί ὶ ϊ ΐ ΐ ΐ ῒ ῒ ἰ Ἰ Ἰ ἱ Ἱ ἴ ἴ Ἴ Ἴ ἵ ἵ Ἵ Ἵ ἳ ἳ ῖ ἶ ἶ ἷ ἷ ό ό ὸ ὀ Ὀ Ὀ ὁ Ὁ ὄ ὄ Ὄ Ὄ ὅ ὅ ὂ ὂ Ὅ ὃ ὃ Ὃ Ὃ Ὃ ῥ Ῥ ̔Ρ ύ ύ Ύ ὺ ϋ ΰ ΰ ΰ ῢ ῢ ὐ ὑ Ὑ ὔ ὔ ὒ ὒ ὕ ὕ ὓ ὓ ῦ ὖ ὖ ὗ ὗ ώ ώ ὼ ῷ ῷ ὠ Ὠ ὡ Ὡ ὤ ὤ Ὤ ὢ ὢ ὥ ὥ Ὥ Ὥ ᾦ ᾧ ᾧ Ὧ ᾯ ᾯ ῶ ῳ ῴ ῴ ὦ ὦ Ὦ ὧ ὧ ὧ ᾠ ᾠ   
* Glyphs NOT used for Greek include:  
; ' ᾿ ` ῾ ’ ‘ ‛ ′ ΄ ʹ̛̀́̓̒̓̔̕ ʹ ʻ ʼ ʽ ʾ ʿ ˈ ˊ ˋ ' ` ´ o ά ὰ ᾷ ἀ Ἀ ἁ Ἁ ἄ Ἄ ἅ ἂ ἃ ᾶ ᾳ ἆ έ ὲ ἐ Ἐ ἑ Ἑ ἔ Ἔ ἕ Ἕ ἓ ή ὴ ῇ ἠ Ἠ ἡ Ἡ ἤ Ἤ ἢ ἥ Ἢ ἣ ᾗ ῆ ῃ ῄ ἦ Ἦ ᾖ ἧ ᾐ ᾑ ᾔ i ί ὶ ϊ ΐ ῒ ἰ Ἰ ἱ Ἱ ἴ Ἴ ἵ Ἵ ἳ ῖ ἶ ἷ ό ὸ ὀ Ὀ ὁ Ὁ ὄ Ὄ ὅ ὂ Ὅ ὃ Ὃ ῥ Ῥ ύ ὺ ϋ ΰ ῢ ὐ ὑ Ὑ ὔ ὕ ὒ ὓ ῦ ὖ ὗ ώ ὼ ῷ ὠ ὡ Ὡ ὤ Ὤ ὢ ὥ Ὥ ᾦ ᾧ ᾯ ῶ ῳ ῴ ὦ Ὦ ὧ Ὧ ᾠ ϛ   
