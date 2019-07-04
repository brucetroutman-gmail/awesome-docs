get HTML with cmd+s or httrack
`httrack '-*' 'https://docs.imade3d.com/Guide/test/810' '+*/*.mp4' '+*/*.medium' --depth=4 --advanced-progressinfo --can-go-up-and-down --display --keep-alive --mirror --mirrorlinks --robots=0 --verbose`

this does get .medium files, but not the huge ones...

can rename with 

`for name in *.medium*; do mv "$name" "${name%.*}.jpg"; done`

and move with
`find *.jpg -type f -print0 | xargs -0 -I {} mv {} ../images`

get JSON from postman 
get the .huge and .medium and .mp4 links from postman
exctract get the links

use http://www.molbiotools.com/textextractor.html with `https.*huge|http.*mp4|http.*medium` 

download all files with wget
wget -i filename.txt
and 
```
for name in *.huge*
    do mv "$name" "${name%.*}.jpg"
done
```
```
for name in *.medium*
    do mv "$name" "${name%.*}.jpg"
done
```

then clean the html with [https://html-cleaner.com/](<https://html-cleaner.com/>)

then convert to md with [https://domchristie.github.io/turndown/](<https://domchristie.github.io/turndown/>)

