# LDSHymns

This repository contains a JSON file with metadata on the LDS Hymns from https://www.lds.org/music/library/hymns.

The `hymns.json` file contains every hymn in the green LDS hymnal keyed by song number faciliating easy hymn lookup. Javascript example: `hymns[301].name // "I Am a Child of God"`

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
