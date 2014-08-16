## Stemmer

This is a mirror of the [snowball](http://snowball.tartarus.org/) stemmer bindings for [Go](http://golang.org/) from [bitbucket.org/tebeka/snowball](https://bitbucket.org/tebeka/snowball) by Miki Tebeka. The mirror was made on 2014-07-25, with the last update by Miki on 2013-07-03. I have copied it here so I don't lose it, just in case, since it is very useful for my own Go [Classifier](https://github.com/AlasdairF/Classifier). I've also added clearer usage instructions in this readme to make it easier to understand the usage.


## Installation

This isn't the only set of C bindings for Go around, but I like this version because it includes all of the C files in the package. No messing around. You can import it with:

`go get github.com/AlasdairF/Stemmer`

*or*

`go get bitbucket.org/tebeka/snowball`


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

Note that the strings you are stemming must not be in CAPITALS, though it is OK if the first letter is Capitalized. Only strings are accepted, not []byte.

    english, err := snowball.New(`english`)
    if err!=nil {
        panic(err)
    }
    w := english.Stem(`testing`)
    fmt.Println(`testing =`,w)
    // testing = test



## Original Readme

[Snowball](http://snowball.tartarus.org/) Stemmer for Go.

For bugs, comments, sources and more - head over to
[https://bitbucket.org/tebeka/snowball](https://bitbucket.org/tebeka/snowball).

[Miki Tebeka](mailto:miki.tebeka@gmail.com)

