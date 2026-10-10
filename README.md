# LDSHymns

This repository contains a JSON file with metadata on the LDS Hymns from https://www.lds.org/music/library/hymns.

The `hymns.json` file contains every hymn in the green LDS hymnal keyed by song number faciliating easy hymn lookup. Javascript example: `hymns[301].name // "I Am a Child of God"`

It also includes the 82 English advance-release hymns from [Hymns for Home and Church](https://www.churchofjesuschrist.org/study/music/hymns-for-home-and-church?lang=eng), verified on 10 October 2026 (1001–1072 and 1201–1210). These entries use the same fields as the original hymnal. `url` and `mp3` link to the choir recording when available, otherwise the children's or solo vocal recording; `alturl` links to piano accompaniment. `pdf`, `midi`, and `playerlink` use the official Music Library resources. `video1`, `video2`, and `songid` are `null` because the current source provides no videos or legacy song identifiers. `bookFilter` is `hymns-for-home-and-church`.

The `hymns.json` file can be used directly without having to host the file yourself using [RawGit](https://rawgit.com) as it uses CORS headers.

Basic jQuery Example using [RawGit.com](https://rawgit.com):

    var hymnURL= 'https://cdn.rawgit.com/pseudosavant/LDSHymns/83bdcf9cce634e61f76aa879fb490e2f64b9d768/hymns.json';
    $.getJSON(
      hymnURL,
      function (hymns){
        // Do something with the hymns
        console.log(hymns);
      }
    )

This is a JSBin example that leverages RawGit: http://output.jsbin.com/xopode
