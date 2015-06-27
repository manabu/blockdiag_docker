# blockdiag_docker

0.2.0

# How to use

```
docker run --rm -v $PWD:/work  -t manabu/blockdiag:0.2.0 blockdiag *.diag
```

# sample

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
