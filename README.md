# blockdiag_docker

0.2.0

# How to use

You can run this container one/off or you can run this container interactively:

```
$ docker run -it --rm -v $PWD/examples:/work manabu/blockdiag-docker bash
root@f0b2c9f9870c:/work# ls
network.nwdiag	sequence.seqdiag  servers.rackdiag  simple.actdiag  tcp-header.packetdiag
root@f0b2c9f9870c:/work# rackdiag
Usage: rackdiag [options] infile

Options:
  --version             show program's version number and exit
  -h, --help            show this help message and exit
  -a, --antialias       Pass diagram image to anti-alias filter
  -c FILE, --config=FILE
                        read configurations from FILE
  --debug               Enable debug mode
  -o FILE               write diagram to FILE
  -f FONT, --font=FONT  use FONT to draw diagram
  --fontmap=FONT        use FONTMAP file to draw diagram
  --no-transparency     do not make transparent background of diagram (PNG
                        only)
  --size=SIZE           Size of diagram (ex. 320x240)
  -T TYPE               Output diagram as TYPE format
  --nodoctype           Do not output doctype definition tags (SVG only)
root@f0b2c9f9870c:/work#
```


## blockdiag

```sh
$ docker run --rm -v $PWD/examples:/work  -t manabu/blockdiag:0.2.0 blockdiag *.diag
```

## rackdiag

```sh
docker run --rm -v $PWD/examples:/work manabu/blockdiag-docker rackdiag -T svg *.rackdiag
```

## nwdiag

```sh
docker run --rm -v $PWD/examples:/work manabu/blockdiag-docker nwdiag -T svg *.nwdiag
```

## seqdiag

```sh
docker run --rm -v $PWD/examples:/work manabu/blockdiag-docker seqdiag -T svg *.seqdiag
```

## acktdiag

```sh
docker run --rm -v $PWD/examples:/work manabu/blockdiag-docker actdiag -T svg *.actdiag
```

## packetdiag

```sh
docker run --rm -v $PWD/examples:/work manabu/blockdiag-docker packetdiag -T svg *.packetdiag
```

# interactive tool

- http://interactive.blockdiag.com/


# docs

- http://blockdiag.com/en/blockdiag/examples.html
- http://blockdiag.com/en/nwdiag/
- http://blockdiag.com/en/seqdiag/examples.html
- http://blockdiag.com/en/actdiag/index.html

- http://blockdiag.com/en/nwdiag/demo.html




## UTF-8

[出力サンプル — blockdiag 1.0 ドキュメント](http://blockdiag.com/ja/blockdiag/examples.html#mutlilingualization "出力サンプル — blockdiag 1.0 ドキュメント")


```
blockdiag admin {
   // Set M17N text using label property.
   A [label = "起"];
   B [label = "承"];
   C [label = "転"];
   D [label = "結"];

   A -> B -> C -> D;

   // Use M17N text directly (need to quote).
   春 -> 夏 -> 秋 -> 冬;

   // Use M17N text including symbol characters (need to quote).
   "春は 曙" -> "夏 = 夜" -> "秋.夕暮れ" -> "冬 & つとめて";
}
```

# License
MIT License
