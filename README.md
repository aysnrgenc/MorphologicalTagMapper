# MorphologicalTagMapper
Tag Mapper to convert morphological analysis tags to Turkish. This is a simple tag mapper for root "araba"

## Setup Finite State Morphology
Please visit download page in url and download version for your platform.
https://web.stanford.edu/~laurik/.book2software/publishing_this_url_is_probited_by_the_license_you_accepted_getting_here_from_the_previous_page.html

## Build Lexicon
Download convertToTurkish.txt and analyzer.lex.txt into your xfst directory and cd directory of xfst
```
./lexc
compile-source analyzer.lex.txt
source-to-result
save-result analyzer.fst
```

## Running Tag Mapper 
```
./xfst -f convertToTurkish.txt
./lookup final.fst
```

## Lookup
Please type i as "I", ex: arabalarInIN
Sample output:
```
 % ./lookup final.fst

  *****  LEXICON LOOK-UP  *****

araba
araba	araba	+Ad+tekil+iyeliksiz+yalin

arabada
arabada	araba	+Ad+tekil+iyeliksiz+de_Hal

arabalarInIn
arabalarInIn	araba	+Ad+cogul+iye_3_T+ilgi_Eki
arabalarInIn	araba	+Ad+cogul+iye_2_T+ilgi_Eki
arabalarInIn	araba	+Ad+cogul+iye_3_C+ilgi_Eki
arabalarInIn	araba	+Ad+tekil+iye_3_C+ilgi_Eki
```
