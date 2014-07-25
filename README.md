## Stemmer

This is a fork of the snowball stemmer bindings for Go from [bitbucket.org/tebeka/snowball](https://bitbucket.org/tebeka/snowball) by Miki Tebeka. The fork was made on 2014-07-25, with the last update by Miki on 2013-07-03. I have copied it here so I don't lose it, just in case, since it is very useful for my own Go [Classifier](https://github.com/AlasdairF/Classifier).


## Installation

I like Miki's version since it includes all of the C files in the package. You can import it with:

go get github.com/AlasdairF/Stemmer
*or*
go get bitbucket.org/tebeka/snowball


## Stemmer Languages Included

    danish
    dutch
    english
    finnish
    french
    german
    hungarian
    italian
    norwegian
    porter
    portuguese
    romanian
    russian
    spanish
    swedish
    turkish

Note that *porter* is an older version of the *english* stemmer. You should use *english* instead.


## Usage

    english, _ := snowball.New(`english`)
    w := english.Stem(`testing`)
    fmt.Println(`testing =`,w)
    // testing = test


## Original Readme

[Snowball](http://snowball.tartarus.org/) Stemmer for Go.

For bugs, comments, sources and more - head over to
[https://bitbucket.org/tebeka/snowball](https://bitbucket.org/tebeka/snowball).

[Miki Tebeka](mailto:miki.tebeka@gmail.com)

